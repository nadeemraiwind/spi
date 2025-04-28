# Copilot Guidelines

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