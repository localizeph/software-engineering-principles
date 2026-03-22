This guide provides a technical overview of Git branching conventions based on standard industry practices and documentation from GeeksforGeeks and the Conventional Branching specification.

## Technical Standards for Branch Naming

To maintain a readable repository history, apply these specific naming rules before creating a new branch:

* **Case Sensitivity:** Use lowercase characters only. For example, use `feat/login` instead of `Feat/Login`.
* **Word Separation:** Use a single hyphen to separate words. Do not use underscores or spaces, as these can cause issues in certain terminal environments.
* **Trailing Characters:** Do not end a branch name with a hyphen or a slash.
* **Starting Characters:** Always start the branch name with a letter. Avoid starting with numbers or special characters.
* **Length and Clarity:** Keep names brief but descriptive. Furthermore, consider limiting the description to three or four words to ensure the name remains manageable in a technical context.

## Branch Categories and Prefixes

Use the following prefixes to categorize the nature of the work. This structure helps team members understand the intent of the branch before reviewing the code.

| Prefix | Use Case |
| :--- | :--- |
| `feat/` | Introducing new functionality to the application. |
| `fix/` | Correcting a bug or technical error. |
| `hotfix/` | Addressing a critical issue in the production environment. |
| `docs/` | Updating documentation, such as a README or technical wiki. |
| `style/` | Adjusting UI appearance or code formatting without changing logic. |
| `refactor/` | Restructuring existing code to improve internal quality. |
| `perf/` | Implementing changes specifically to improve system performance. |
| `test/` | Adding or updating tests to verify code stability. |
| `chore/` | Performing routine maintenance, such as updating dependencies. |

## Standard Naming Patterns

### General Task Pattern
This pattern is appropriate for general updates:
`type/description-of-work`
* `feat/api-connection`
* `style/header-colors`

### Ticket-Based Pattern
For teams using project management software, including the ticket ID is often required:
`type/id-description`
* `fix/bug-104-login-timeout`
* `feat/task-202-user-profile`

## Recommendations for Clean Repositories

In conclusion, following these patterns prevents common issues relative to repository management. Consider the following points:

1.  **Avoid Personal Identifiers:** Do not use your name as a branch prefix. Git tracks the author of the branch automatically, making personal names redundant.
2.  **Avoid Vague Descriptions:** Terms like `update`, `fix`, or `temp` lack technical detail and make it difficult for others to understand the branch's purpose.
3.  **Merge and Delete:** Technical workflows are more efficient when branches are short-lived. Delete the branch after the merge is complete to keep the remote repository organized.
