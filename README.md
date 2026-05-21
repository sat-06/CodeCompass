## Project Architecture

The system follows a simple recommendation workflow where the user provides project preferences, the backend processes those inputs, compares them with the project dataset, and returns the most suitable project recommendations.

```mermaid
flowchart TD
    A[User] --> B[Frontend UI]

    B --> C[Input Form]
    C --> C1[Tech Domain]
    C --> C2[Skills]
    C --> C3[Available Hours]
    C --> C4[Difficulty Level]

    C --> D[Backend API]

    D --> E[Input Processing]
    E --> F[Recommendation Engine]

    G[Project Dataset] --> F

    F --> H[Project Matching Logic]
    H --> I[Rank Projects by Match Score]

    I --> J[Top Recommended Projects]

    J --> K[Project Details Page]
    K --> K1[Project Title]
    K --> K2[Description]
    K --> K3[Required Skills]
    K --> K4[Estimated Time]
    K --> K5[Difficulty Level]

    K --> L[User Selects a Project]