# JFrame-Banking-System
simple basic Banking System transaction Deposit, Withdrawal, and sending money
# Banking System - Java Swing

A simple 2-JFrame desktop banking application built in Java Swing and Apache NetBeans.

## Overview
The application consists of two connected JFrames: **System** for authentication and **bank** for transactions. The user must login first to access the banking dashboard.

## System Workflow
`System.java (Login)` -> `bank.java (Dashboard)`

## Modules

### 1. System - Login Module
The entry point and security gate of the application.

**UI Components:**
- `txtname` - JTextField for Name input
- `txtpin` - JTextField for PIN input
- `lbl` - JLabel for error messages
- `log` - LOGIN button
- `clear` - CLEAR button
- `exit` - EXIT button

**Functionality:**
- Validates user with hardcoded credentials.
- **Name:** `Tumisang`
- **PIN:** `1234`
- On success: Opens `bank` JFrame and disposes current frame.
- On failure: Displays "Invalid Input!" on the label.

**Core Code:**
```java
// LOGIN
String Name = txtname.getText().trim();
String Pin = txtpin.getText().trim();
if(Name.equalsIgnoreCase("Tumisang") && Pin.equalsIgnoreCase("1234")){
    new bank().setVisible(true);
    this.dispose();
} else {
    lbl.setText("Invalid Input!");
}

// CLEAR
txtname.setText("");
txtpin.setText("");

// EXIT
System.exit(0);
