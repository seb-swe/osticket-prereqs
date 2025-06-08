<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" />
</p>

# osTicket - Prerequisites and Installation Lab

This lab outlines the prerequisites and step-by-step installation process for the open-source help desk ticketing system **osTicket** on a Windows IIS environment.

---

## Environments and Technologies Used

- Microsoft Azure (Virtual Machines / Compute)
- Remote Desktop Protocol (RDP)
- Internet Information Services (IIS)
- PHP Manager for IIS
- MySQL Server
- HeidiSQL (Database Management Tool)

---

## Operating System

- Windows 10 (21H2)

---

## List of Prerequisites

- Azure Virtual Machine running Windows 10
- IIS Web Server with CGI support
- PHP (7.x or 8.x recommended)
- Microsoft Visual C++ Redistributable
- MySQL Server (8.x recommended)
- PHP Manager for IIS
- IIS URL Rewrite Module 2

---

## Installation Steps

### 1. Download and Extract osTicket Files

![Step 1](https://github.com/user-attachments/assets/2710c685-4615-4ee6-90ab-6f55a5b8804a)
- Downloaded and extracted the osTicket files onto the VM desktop.
- The folder contains all dependencies required for osTicket.

---

### 2. Install IIS and Required Features

![Step 2](https://github.com/user-attachments/assets/fe16da85-401c-4191-a4a9-e26a49e3b76e)
- Installed IIS (Internet Information Services) to provide core web server functionality to host osTicket.
- Installed Web Management Tools for IIS to enable easy graphical configuration.
- Installed World Wide Web Services with CGI to process dynamic content and run server-side scripts.

---

### 3. Install PHP Manager and IIS URL Rewrite Module

![Step 3](https://github.com/user-attachments/assets/f7418b73-8047-41d7-af09-7c0156330c6e)
![Step 3-2](https://github.com/user-attachments/assets/67ab74c0-30d5-439b-9a84-51fc9cd6afa7)
- Installed PHP Manager to simplify PHP configuration and management on IIS, ensuring osTicket runs smoothly with required PHP settings and extensions.
- Installed IIS URL Rewrite Module 2 to enable clean, user-friendly URLs and proper routing, improving site accessibility and SEO.

---

### 4. Create PHP Installation Directory

![Step 4](https://github.com/user-attachments/assets/49d36380-9581-42d5-b0fd-2ce4ed2a8370)
- Created the `C:\PHP` directory as a dedicated location for PHP installation, ensuring IIS can properly locate and run PHP scripts for osTicket.

---

### 5. Install Required Software

![Step 5](https://github.com/user-attachments/assets/3f901788-0367-4de9-b705-815752ad6f02)
![Step 5-2](https://github.com/user-attachments/assets/257fbf52-6f96-4f0f-9c44-8a807df9344c)
- Installed Microsoft Visual C++ Redistributable to provide necessary runtime libraries for PHP and its extensions.
- Installed MySQL Server to provide the database backend for storing and managing osTicket data.

---

### 6. Register PHP Version in IIS

![Step 6](https://github.com/user-attachments/assets/2a32b287-14ca-4ad9-8579-0bb9398ef019)
- Registered a new PHP version in IIS to ensure the web server uses the correct PHP runtime to execute osTicket’s scripts.

---

### 7. Deploy osTicket Files to IIS Web Root

![Step 7](https://github.com/user-attachments/assets/e1eed563-0d32-4788-8ab1-2d227c3ec117)
- Copied the `upload` folder to `C:\inetpub\wwwroot` and renamed it to `osTicket` to place application files in the web server’s root directory for public access.

---

### 8. Enable Required PHP Extensions

![Step 8](https://github.com/user-attachments/assets/9a85ca98-eeb7-4d15-be5d-49037d25d72a)
- Enabled `php_imap.dll`, `php_intl.dll`, and `php_opcache.dll` extensions in PHP Manager to support email handling, internationalization, and performance optimization for osTicket.

---

### 9. Configure osTicket Configuration File and Permissions

![Step 9](https://github.com/user-attachments/assets/af367257-0159-4431-906e-d65159b40eb5)
![Step 9-2](https://github.com/user-attachments/assets/59a61c61-5a28-49b6-aa0f-cd984e97f70b)
- Renamed `ost-sampleconfig.php` to `ost-config.php` to activate the osTicket configuration file required for the application to run.
- Configured file permissions on `ost-config.php` by disabling inheritance and granting full access to Everyone to ensure proper read/write access.

---

### 10. Setup Database Using HeidiSQL

![Step 10](https://github.com/user-attachments/assets/eb9df101-5552-4fd5-9854-d62ad281555c)
![Step 10-2](https://github.com/user-attachments/assets/09cb59ce-03d7-4e4c-9fda-93c89905f4da)
- Installed HeidiSQL to provide a user-friendly interface for creating and managing the osTicket MySQL database.

---

### 11. Complete osTicket Web Installation

- Opened the web browser and navigated to the osTicket setup page.
- Provided MySQL database credentials:
  - Database: `osTicket`
  - Username: `root`
  - Password: `root`
- Clicked **Install Now!** to complete the setup and connect osTicket to the database.

---

## Conclusion

This lab demonstrates practical skills in deploying osTicket on a Windows IIS server within an Azure VM environment. It covers critical tasks such as IIS and PHP configuration, MySQL database setup, file permission management, and application deployment. Successfully completing this lab highlights the ability to install and configure enterprise-grade help desk solutions, ensuring proper security, performance, and maintainability in a real-world IT environment.

