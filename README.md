# Edmire.ai <span style="font-size: 0.6em; font-style: italic">(For ERPNext)</span>

 Elevating Education Management with ERPNext Excellence.

## Table of Contents
 - [Pre-requisites](#pre-requisites)
 - [Introduction](#introduction)
 - [Key-Features](#Key-Features)
    - [Administration](#Administration)
    - [Admission Registration](#Admission-Registration)
    - [Academic Management](#Academic-Management)
    - [Examination Planning](#Examination-Planning)
    - [Examination Registration](#Examination-Registration)
    - [Secure and Fair Evaluation](#Secure-and-Fair-Evaluation)
    - [User-Friendly Interface](#User-Friendly-Interface)
  - [Installation](#Installation)
  - [Resources](#resources)
  - [License](#license)


## Pre-requisites
* Python 3.6+
* Frappe
* ERPNext


## Introduction
Welcome to Edmire.ai

Edmire.ai is a cutting-edge Education Management System, meticulously crafted to enhance the administrative and academic processes of educational institutions. Inspired by the principles of open-source innovation, our platform is built on the robust ERPNext software foundation, ensuring reliability and flexibility.

Our vision at Edmire.ai is to revolutionize education management, offering a bespoke and user-friendly solution. We aim to simplify and streamline processes, making them more efficient for educational institutions. With a powerful module that inherits the strengths of the ERPNext framework, Edmire.ai provides a solid foundation tailored to meet the unique needs of your institution.


## Key-Features

### Administration
Edmire.ai empowers administrators with a suite of tools to efficiently manage various administrative tasks, reducing manual intervention and enhancing overall operational efficiency. From staff management to resource allocation, Edmire.ai ensures streamlined administrative processes.

### Admission Registration
Simplify and expedite the student admission process with Edmire.ai. Our module streamlines the admission registration process, capturing accurate and up-to-date information. Define admission criteria and seamlessly manage the entire admission workflow.

### Academic Management
Edmire.ai caters to the needs of educators by providing robust tools for managing courses, curriculum, and student information. It fosters a structured and effective learning environment, promoting academic excellence.

### Examination Planning
Effortlessly plan and organize examinations with Edmire.ai. From scheduling exams to creating question paper sets and managing seating arrangements, our module ensures a comprehensive solution for all your examination planning needs.

### Examination Registration
Streamline the student registration process for examinations using Edmire.ai. Capture crucial information and generate admit cards based on predefined criteria, ensuring a smooth and organized examination registration process.

### Secure and Fair Evaluation
 Edmire.ai places a premium on the integrity of the examination process. Benefit from features designed for secure paper setting, digital evaluation, and result processing, ensuring a fair and reliable assessment system.
 
### User-Friendly Interface
 Prioritizing user experience, Edmire.ai offers an intuitive interface for educators, students, and administrators. Simple navigation enhances accessibility, enabling users to effortlessly access the information and tools they need for a seamless experience.

1. Setup dependencies
    ```
    cd biometric-attendance-sync-tool
      && python3 -m venv venv
      && source venv/bin/activate
      && pip install -r requirements.txt
    ```

## Installation
- You need to make a copy of `local_config.py.template` file and rename it to `local_config.py`
- Please fill in the relevant sections in this file as per the comments in it.
- Below are the delineation of the keys contained in `local_config.py`:
  - ERPNext connection configs:
    - `ERPNEXT_API_KEY`: The API Key of the ERPNext User
    - `ERPNEXT_API_SECRET`: The API Secret of the ERPNext User

      > Please refer to [this link](https://frappe.io/docs/user/en/guides/integration/how_to_set_up_token_based_auth#generate-a-token) to learn how to generate API key and secret for a user in ERPNext.
      > The ERPNext User who's API key and secret is used, needs to have at least the following permissions:
      > 1. Create Permissions for 'Employee Checkin' DocType.
      > 2. Write Permissions for 'Shift Type' DocType.

    - `ERPNEXT_URL`: The web address at which you would access your ERPNext. eg:`'https://yourcompany.erpnext.com'`, `'https://erp.yourcompany.com'`
    - `ERPNEXT_VERSION`: The base version of your ERPNext app. eg: 12, 13, 14
  - This script's operational configs:
    - `PULL_FREQUENCY`: The time in minutes after which a pull for punches from the biometric device and push to ERPNext is attempted again.
    - `LOGS_DIRECTORY`: The Directory in which the logs related to this script's whereabouts are stored.
      > Hint: For most cases you can leave the above two keys unchanged.
    - `IMPORT_START_DATE`: The date after which the punches are pushed to ERPNext. Expected Format: `YYYYMMDD`.
      > For some cases you would have a lot of old punches in the biometric device. But, you would want to only import punches after certain date. You could set this key appropriately. Also, you can leave this as `None` if this case does not apply to you.

> TODO: fill this section with more info to help Non-Technical Individuals.

## To build executable file for GUI
### Linux and Windows:
1. Activate virtual environment.
1. Navigate to the repository folder (where `gui.py` located) by
    ```
    cd biometric-attendance-sync-tool
    ```
1. Run the following commands:
    ```
    pip install pyinstaller
    ```

    ```
    python -m PyInstaller --name="attendance-sync" --windowed --onefile gui.py
    ```
1. The executable file `attendance-sync` created inside `dist/` folder.

### Resources

* Article on [ERPNext Documentation](https://docs.erpnext.com/docs/user/manual/en/setting-up/articles/integrating-erpnext-with-biometric-attendance-devices).
* This Repo's [/Wiki](https://github.com/frappe/biometric-attendance-sync-tool/wiki).

### License

This project is licensed under [GNU General Public License v3.0](LICENSE)
