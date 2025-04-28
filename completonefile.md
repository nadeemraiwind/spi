
## General Guidelines
1. **Stick to the Stack**: Use only PHP, JavaScript, CSS, HTML, and MySQL for all development tasks.
2. **Code Organization**: Follow the project structure outlined in the `README.md` file. Keep the code clean and modular.
3. **Database Configuration**: Ensure all database-related changes are reflected in `src/config/database.php`.
4. **Testing**: Test all new features thoroughly before committing changes.

## Updating the Project
1. **Adding/Updating/Deleting Files**:
   - When adding, updating, or deleting any page, file, feature, or functionality, ensure all related files are updated accordingly.
   - Update the `FEATURES.md` file to reflect the changes.
   - If the change affects the project structure, update the `README.md` file.

2. **Documentation**:
   - Document all new features and changes in the appropriate files.
   - Ensure comments in the code are clear and concise.

3. **Version Control**:
   - Commit changes with meaningful commit messages.
   - Use branches for new features or bug fixes and merge them into the main branch after review.

## Best Practices
1. **Clear Comments and Descriptions**
   - Write clear and concise comments in your code to help Copilot understand the context.
   - Use descriptive function and variable names to improve code readability.

2. **Use Specific Prompts**
   - When asking Copilot for code suggestions, be specific about what you need. For example, instead of asking for "a function," specify "a function to validate email addresses."

3. **Review Suggestions Carefully**
   - Always review the code suggestions provided by Copilot. Ensure that the generated code meets your project requirements and adheres to best practices.

4. **Iterative Development**
   - Use Copilot in an iterative manner. Start with a basic implementation and refine it with Copilot's suggestions.

5. **Leverage Context**
   - Provide Copilot with as much context as possible. This includes relevant code snippets, comments, and documentation.

6. **Test Generated Code**
   - After implementing suggestions from Copilot, thoroughly test the code to ensure it functions as expected and does not introduce bugs.

7. **Stay Updated**
   - Keep abreast of updates and improvements to Copilot. New features may enhance its capabilities and your development workflow.

8. **Collaborate with Team Members**
   - Share Copilot-generated code with your team for feedback and collaborative improvement. This can lead to better solutions and learning opportunities.

9. **Update Files Consistently**
   - When adding, updating, or deleting any page, file, feature, or functionality:
     - Ensure all related files are updated accordingly.
     - Update the `FEATURES.md` file to reflect the changes.
     - If the change affects the project structure, update the `README.md` file.
     - Document the changes clearly in the code and relevant documentation.

10. **Ensure Android Compatibility**
    - Design the backend to expose RESTful APIs for future Android app integration.
    - Use token-based authentication (e.g., JWT) for secure communication between the backend and the Android app.
    - Keep the database schema optimized for scalability and mobile app compatibility.
    - Separate frontend logic from backend logic to ensure seamless integration with the Android app.

## New Feature Development
1. **Follow Modular Design**:
   - Ensure new features are implemented as self-contained modules.
   - Place all module-related files in the `src/core/modules/` directory.

2. **API Integration**:
   - Document all new API endpoints in `technical-documentation.md`.
   - Ensure APIs follow RESTful principles and are secured with token-based authentication.

3. **Testing Requirements**:
   - Write unit tests for all new features using PHPUnit.
   - Ensure integration tests cover interactions between modules and core systems.

## Contribution Workflow
1. Fork the repository and create a new branch for your changes.
2. Make your changes and test them locally.
3. Submit a pull request with a detailed description of the changes.

## Conclusion
By following these guidelines, you can maximize the benefits of using GitHub Copilot in your PHP project. Embrace the tool as a collaborative partner in your development process, and always prioritize code quality and maintainability.
# My PHP Project

## Overview
This project is a modular web application built using PHP, JavaScript, CSS, HTML, and MySQL. It is designed to provide a robust and dynamic user experience while maintaining a clean and organized code structure. The backend is designed to expose RESTful APIs for future Android app integration.

## Project Structure
The project is organized as follows:

```
my-php-project
├── src
│   ├── core
│   │   ├── assets                # Contains CSS, JS, and image files for the core application
│   │   │   ├── css               # Core CSS files
│   │   │   ├── js                # Core JavaScript files
│   │   │   └── images            # Core image assets
│   │   ├── config                # Configuration files for the core application
│   │   │   ├── database.php      # Database connection settings
│   │   │   └── globalconfig.php  # Global configuration file for app settings, debug mode, etc.
│   │   ├── templates             # Core templates for admin views
│   │   │   ├── admin-header.php  # Admin header template
│   │   │   ├── admin-footer.php  # Admin footer template
│   │   │   └── dashboard.php     # Admin dashboard template
│   │   ├── modules               # Directory for dynamically added modules
│   │   │   └── (empty for now, modules will be added here)
│   │   ├── admin.php             # Admin dashboard entry point
│   │   ├── Kernel.php            # Application kernel for bootstrapping the app
│   │   ├── Router.php            # Routing system for handling requests
│   │   ├── ModuleLoader.php      # Module loader for dynamic module management
│   │   └── Database.php          # Database handling system using PDO
│   ├── user
│   │   ├── assets                # Contains CSS, JS, and image files for the user application
│   │   │   ├── css               # User CSS files
│   │   │   ├── js                # User JavaScript files
│   │   │   └── images            # User image assets
│   │   ├── templates             # User templates for user views
│   │   │   ├── user-header.php   # User header template
│   │   │   ├── user-footer.php   # User footer template
│   │   │   └── user-dashboard.php # User dashboard template
│   │   └── index.php             # User dashboard entry point
├── api
│   ├── v1                        # API version 1
│   │   ├── users.php             # API for user-related operations
│   │   ├── modules.php           # API for module-related operations
│   │   └── auth.php              # API for authentication
├── copilot-guidelines.md         # Guidelines for using GitHub Copilot in this project
├── FEATURES.md                   # Checklist of implemented and planned features
├── technical-documentation.md    # Technical documentation for APIs and other details
└── README.md                     # Project overview and setup instructions
```

## Setup Instructions
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/your-repo/my-php-project.git
   ```
2. Navigate to the project directory:
   ```bash
   cd my-php-project
   ```
3. Set up the MySQL database:
   - Import the SQL file located at `src/core/config/schema.sql` into your MySQL server.
   - Update the database credentials in `src/core/config/database.php`.
4. Run the application kernel (`src/core/Kernel.php`) to initialize the system:
   ```bash
   php src/core/Kernel.php
   ```
5. Open the application in your browser:
   - Admin Dashboard: `http://localhost/core/admin.php`
   - User Dashboard: `http://localhost/user/index.php`

## Usage
- The application is designed to be modular. Modules can be added dynamically to extend functionality.
- RESTful APIs are available for core functionalities to support future Android app integration.
- The app includes a kernel system, routing system, modular system, and database handling system for scalability and maintainability.
- Refer to the `FEATURES.md` file for a checklist of implemented features and future enhancements.

## Contributing
Contributions are welcome! Please follow the guidelines in `copilot-guidelines.md` for best practices when contributing to this project.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Recent Updates
- Added `globalconfig.php` for centralized app settings and global functions.
- Modular design guidelines have been added to the contribution workflow.
- API documentation requirements are now included in `technical-documentation.md`.
- Testing requirements for new features are outlined in `copilot-guidelines.md`.

## Contribution Highlights
- Follow the modular design principles for new features.
- Document all API changes in `technical-documentation.md`.
- Ensure all new features are thoroughly tested before submission.
```

Let me know if you need further updates or adjustments!

# Features Checklist

## Core Features
- [x] Modular application system with dynamic module installation.
- [x] Basic routing system for core and module pages.
- [x] User authentication (login, registration).
- [x] Database connection setup in `src/config/database.php`.
- [x] Admin dashboard for managing modules and settings.
- [x] Basic UI for the main app (admin interface).
- [x] Basic UI for the user app (user dashboard).
- [x] RESTful APIs for core functionalities (e.g., user authentication, module management).
- [x] Kernel system to bootstrap and manage the app lifecycle.
- [x] Database handling system using PDO for secure and efficient queries.

## Planned Features
- [ ] Module installation system with validation and registration (detailed plan added in technical documentation).
- [ ] Role-based access control (RBAC) for managing user permissions (design strategy added in technical documentation).
- [ ] Centralized logging and error-handling system (example integration added in technical documentation).
- [ ] Document all API endpoints using Swagger or Postman (setup and maintenance details added in technical documentation).
- [ ] Plan for Android app features like push notifications, offline support, and real-time updates (expanded backend support details added in technical documentation).

## Maintenance Checklist
- [ ] Ensure all files are updated when adding, updating, or deleting features.
- [ ] Keep the `README.md` and `FEATURES.md` files up to date.
- [ ] Regularly review and refactor code for optimization.
- [ ] Ensure all CSV files, fonts, and other assets are stored within the project directory for easy access and maintenance.