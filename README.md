# CompanyDashboard

## Project Overview
CompanyDashboard is a Vue.js project to improve my skills in frontend developing.

## Project Structure
```
CompanyDashboard/
├─ src/                         # Source code/Components
│   └── components/             # Repository with components
        └──Header.vue           # Header component
        └──HeaderButton.vue     # HeaderButton component
        └──Stat.vue             # First block Stat component
        └──StatInfo.vue         # Popup for Stat component
        └──StatList.vue         # List of Stat components
        └──Text.vue             # Component for Stat filling
├── main.js                  # Main JavaScript script
├── index.html               # Main html file to enter script
├── package.json             # Setting to run the project
├── .gitignore               # Git ignore file
├── README.md                # Project documentation
```

## Branching Strategy
This project follows the Git Flow branching model:
- `main`: The production-ready branch.
- `dev`: The development branch where features are integrated.
- `feature/*`: Feature branches for developing new features.

## Getting Started

### Installation
1. Clone the repository:
    ```
    git clone git@github.com:Evgeninio/CompanyDashboard.git
    cd CompanyDashboard
    ```

2. Initialization packet manager
    ```
    npm init
    ```

### Running the Project
    ```
    npn run dev  # Start project on a local-server
    ```