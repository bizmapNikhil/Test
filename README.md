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

1. Install Frappe bench on your local machine 
2. After installing frappe bench Install ERPNext
3. After installing the frappe and erpnext then install the Education app
4. Once the Frappe bench, ERPNext and Education is installed, install the Edmire.ai App by using  
        ```  $bench get-app edmire.ai  ```
5. After that you can install the Edmire.ai app on the required site by running
        ```   $ bench –site sitename install-app edmire.a ```



### Resources

* Article on [ERPNext Documentation](https://docs.erpnext.com/docs/user/manual/en/setting-up/articles/integrating-erpnext-with-biometric-attendance-devices).
* This Repo's [/Wiki](https://github.com/frappe/biometric-attendance-sync-tool/wiki).

### License

This project is licensed under [GNU General Public License v3.0](LICENSE)
