## Updated Project Documentation: School Batch 2003 Directory

**Project Overview**  
This project aims to create a digital directory for the 2003 batch of a school, allowing alumni to sign up, manage profiles, and register for events. Admin users will manage events and payment statuses from a backend dashboard.

### Project Requirements

---

### 1. **User Authentication**
   - **Sign Up Form**
     - **Fields** (All required):
       - First Name
       - Last Name
       - Email
       - Phone Number
     - **Phone Number Visibility**: Checkbox to toggle between "Public" and "Private."
     - **Security**: reCAPTCHA integration.
   - **Sign In Form**
     - Users must be able to log in using email and password.

---

### 2. **User Profile**
   - **Profile Information**
     - Fields available for user input:
       - First Name, Last Name, Email, Phone Number (editable)
       - **Occupation** (with conditional fields):
         - **If Job/Service**: Show fields for Job Title and Company.
         - **If Business**: Show a field for Business Name.
       - Blood Group
       - Profile Photo (upload)
       - Social Media Links (optional)
     - **Phone Number Visibility**: Users can set visibility to Public or Private.
   - **Edit/Update Profile**: Users should be able to update any information in their profile at any time.

---

### 3. **Directory Listing**
   - **Columns in Directory List:**
     - Full Name
     - Email
     - Phone Number:
       - Visibility controlled by each user. If set to private, display as masked (e.g., "******").
     - Blood Group
     - **Action Icons**: Options to View, Edit, and Delete.
   - **Search, Filter, and Sort**:
     - Directory listing should have search, filter, and sorting functionalities for ease of access.

---

### 4. **Events Management**

   #### Frontend (User View)
   - **Event List**
     - Only signed-in users can view the event list.
     - **Event Details**:
       - Start and End Dates
       - Cover Photo
       - Event Details/Description
       - Payment Options for Registration (Cash, Mobile Banking, Card Payment).
   - **Event Registration Directory**
     - Users who register for events are added to a registration directory with the following columns:
       - Full Name, Email, Phone, Payment Method, Payment Status (Pending/Completed).

   #### Backend (Admin View)
   - **Create/Edit Events**:
     - Admin can create, update, or delete events with the following fields:
       - Event Name
       - Start Date
       - End Date
       - Cover Photo
       - Details/Description
       - Payment Options
   - **Manage Event Registration**:
     - Admin can view who has registered for an event and update payment status for users who selected Cash or Mobile Banking.
     - Ability to filter, sort, and search within the registration list.
   - **Event End Handling**:
     - When an event concludes, the registration table associated with that event should be:
       1. Exported as a PDF document, recording all registered user information (including Full Name, Email, Phone, Payment Method, and Payment Status).
       2. Saved to an application folder for archival purposes.
       3. Deleted from the database to reduce storage of unnecessary data.

---

### 5. **Technology Stack**
   - **Backend**: Laravel
   - **Frontend**: React or Vue.js (open for developer preference)
   - **Database**: MySQL

---

### 6. **User Interface (UI) Guidelines**
   - **User-Friendly Forms**:
     - Ensure all fields are clearly labeled and necessary options (such as toggles and conditional fields) are easy to interact with.
   - **Responsive Design**:
     - Directory and Event listings should be responsive, optimized for both desktop and mobile views.
   - **Event Registration & Payment Status**:
     - Visual indicators for payment status (e.g., badges or color coding for Pending and Completed) to make it easy to identify at a glance.
   - **Admin Dashboard**:
     - Clear layout for creating and managing events, with straightforward access to view and update event registrations and payment statuses.

---

### 7. **Additional Considerations**
   - **Security**: 
     - Ensure secure data handling, especially for profile updates and payment details.
   - **Scalability**:
     - Design the database and code to handle potential future expansions, such as additional alumni batches or more profile customization options.

This document should serve as a comprehensive guideline for developers and designers, allowing them to deliver a complete solution that meets the requirements for the School Batch 2003 Directory.
