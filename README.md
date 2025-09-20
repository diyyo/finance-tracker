# Serverless Static Finance Tracker Web App with Firebase Realtime Database

![License](https://img.shields.io/badge/license-MIT-blue.svg)

A simple, modern, and responsive web-based personal finance tracker application. Built with HTML, Tailwind CSS, and powered by Firebase for authentication and a real-time database.

## 🔑 Key Features

### 👤 User Features
* **Google Authentication:** Log in easily and securely with a Google account.
* **Financial Dashboard:** View a real-time summary of total income, expenses, and balance.
* **Transaction Management (CRUD):** Add, view, edit, and delete income or expense transactions.
* **Search & Filter:** Find transactions by description or filter by type (income/expense).
* **Data Sorting:** Sort transactions by date or amount (newest, oldest, highest, lowest).
* **Saved Descriptions:** Save frequently used descriptions to speed up adding new transactions.
* **Pagination:** Easy navigation for a large number of transactions.
* **Progressive Web App (PWA):** Can be installed on mobile or desktop devices for a native app-like experience.

### 🔒 Administrator Features
* **Admin Panel:** A dedicated page to manage all application data.
* **User Management:** View a list of all users, their status (active/banned), and perform ban/unban actions.
* **Global Transaction Management:** Admins can view, add, edit, and delete transactions for any user.

## ⚙️ Tech Stack

-   Frontend: HTML, CSS, Tailwind CSS, JavaScript 
-   Firebase SDKs: Authentication, Realtime Database
-   Tools: Firebase CLI

## ❔ How to Use?

To run this project in your local environment, follow these steps:

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/diyyo/finance-tracker.git
    cd finance-tracker
    ```

2.  **Create a Firebase Project**
    * Go to the [Firebase Console](https://console.firebase.google.com/).
    * Create a new project.
    * Inside the project, create a new Web App (click the `</>` icon).
    * Copy the provided Firebase configuration (`firebaseConfig`).

3.  **Configure Firebase in the HTML**
    * Open the `index.html` file.
    * Find the `<script>` tag at the bottom that contains `const firebaseConfig`.
    * Replace the existing `firebaseConfig` object with the configuration from your Firebase project.
    ```javascript
    const firebaseConfig = {
        apiKey: "...",
        authDomain: "...",
        databaseURL: "...",
        projectId: "...",
        storageBucket: "...",
        messagingSenderId: "...",
        appId: "...",
        measurementId: "G-..."
    };
    ```

4.  **Enable Google Sign-In**
    * In the Firebase Console, go to the **Authentication** section.
    * Select the **Sign-in method** tab.
    * Enable the **Google** provider.

5.  **Configure Admin (Optional)**
    * To access the admin panel, you need to register your account's UID.
    * Log in to the application once with the account you want to make an admin.
    * Go to the **Firebase Console** -> **Realtime Database**.
    * Create a new data structure with the path: `admin/uid`.
    * Set its value to be an array containing your admin account's UID as a string. Example:
    ```json
    {
      "admin": {
        "uid": [
          "ABcdeFGhIJkLMnOPqRSTuVwxyZ12345"
        ]
      }
    }
    ```

6.  **Run/Deploy the Application**
    * Open the `index.html` file directly in your browser.
    * For the best experience, it's recommended to use an extension like "Live Server" in Visual Studio Code to run a local development server.

## ⚖️ License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.

(c) diyyo White 2025 MIT License.
