# OKR Genius Documentation

## 1. Introduction

"OKR Genius" is an advanced web application designed to help teams and organizations simplify and enhance the process of defining, tracking, and achieving their Objectives and Key Results (OKRs). Using Artificial Intelligence algorithms, the platform offers data-driven OKR suggestions aligned with the organization's business objectives and strategies. Users can customize, track in real-time, and collaborate on OKRs, all within an integrated and secure system. Its operation is based on the following points:

- **Objective Definition**: Begin by setting your organization's overall objectives and goals, specifying what you want to achieve and in what timeframe.
- **AI-Driven Suggestions**: OKR Genius uses advanced artificial intelligence algorithms to analyze business data, historical performance, and industry benchmarks. It then generates suggested OKRs that are realistic, measurable, and align with your goals.
- **Customization**: Customize the generated OKRs to match your organization's unique priorities and strategies. This includes modifying key results, setting target values, and adding context as needed.
- **Alignment**: Ensure all OKRs, both individual and team-based, align with the organization's higher-level goals. OKR Genius assists in breaking down goals across the company.
- **Progress Tracking**: Monitor your OKRs' progress in real time. OKR Genius provides visual dashboards and analytics, allowing you to oversee key outcomes, spot trends, and identify areas needing attention.
- **Data-Driven Insights**: Gain insights into your OKRs' performance and discover patterns that can influence strategic decisions. OKR Genius offers data-driven progress recommendations.
- **Collaboration**: Collaborate with teams and individual members to ensure everyone is working towards common goals. Share OKRs, updates, and feedback within the platform.
- **Integration**: OKR Genius integrates with other business tools and platforms to optimize your workflow and improve data accuracy.
- **Security and Privacy**: Your OKR data is protected and complies with privacy regulations. OKR Genius prioritizes data security and confidentiality.

In summary, OKR Genius uses AI to simplify and enhance OKR management, helping organizations better align their objectives and boost performance. Creating an account is straightforward, and you can securely access your OKRs and performance data on your user profile.

## 2. System Architecture
We decided to use Next.js for its distinctive features:

Automatic Optimization: This feature enhances both the performance and the user experience when interacting with the application.
Server-Side Rendering (SSR): This functionality is essential for gaining benefits in SEO and ensuring fast web loading times.
Integrated API Functions: This integration facilitates communication between the frontend and the backend without requiring additional configurations.
Rapid Development: Thanks to tools like hot reloading, the development process becomes more efficient and agile.
### 2.1. Frontend

The "OKR Genius" application uses Next.js as its frontend framework. The structure is based on pages representing different views in the app, such as "Home", "Profile", and "Dashboard". Next.js API functions are used to communicate with the backend.


### 2.2. Backend

For the backend and data management, we chose MongoDB and Express.js for the following reasons:

Flexible Schema (MongoDB): The absence of a fixed structure in MongoDB provides us with constant adaptability and evolution in data management.
Horizontally Scales (MongoDB): This capability ensures that the application can grow and handle more data simply by adding more resources.
Agile Development (Express.js): With Express.js, we can quickly set up a web server. In addition, its middleware system allows for a modular and extensible structure.

With these technological choices, we aim to guarantee a robust, scalable, and efficient application to meet all the demands and needs of our users.

### 2.3. Database

We use MongoDB as our database. It is structured in collections representing different entities in the system:

- `users`: Stores user information like email, encrypted password, OKRs, and OKRs in PDF format.
- `okrs`: Contains all OKRs generated by users, associated by user ID. Additionally, OKRs are stored in PDF format for easy user download.
- `sessions`: Stores session information for authenticated users.

## 3. Main Features

### 3.1. Authentication

Authentication is managed through Next Auth. When a user registers, their details are stored in the `users` collection. Login checks credentials and generates a JWT token for the session.

### 3.2. OKR Generation

OKRs are generated based on objectives entered by the user and information analyzed by AI algorithms. Once generated, they're stored in the `okrs` collection.

### 3.3. Download OKRs in PDF

We use the "pdf-lib" library to generate PDFs. Users can select OKRs and generate a PDF report for direct download.

### 3.4. OKR History

Past OKRs for each user are stored and can be viewed in a "History" section. Each OKR has an associated date, allowing users to review their progress over time.

## 4. Integrations

"OKR Genius" integrates with the OpenAI API, one of the most advanced programming interfaces in the AI field. This integration is crucial for providing users with AI-based OKR suggestions. By utilizing the OpenAI API, "OKR Genius" can:

- Analyze previously defined goals by organizations and offer optimized OKRs based on historical and current data.
- Recognize patterns and trends from vast datasets, enabling the generation of more relevant OKRs aligned with organizations' current needs.
- Provide ongoing recommendations to adjust and refine OKRs as circumstances or business goals change.

This integration ensures "OKR Genius" remains at the forefront of AI-based OKR management solutions, offering users more accurate and valuable recommendations.

## 5. Deployment

We will deploy "OKR Genius" on Vercel, a leading platform for deploying modern web applications. The deployment steps are:

- **Connect with Vercel**: Start by linking your "OKR Genius" repository to Vercel. This is done through an intuitive interface where you select the desired repository and grant Vercel access.
- **Environment Variables Configuration**: Before deploying, it's essential to set up environment variables in Vercel. This includes, but is not limited to, MongoDB credentials and OpenAI API access keys. These variables ensure the app operates correctly in the production environment.
- **Initiate Deployment**: Once everything is set up, you can begin the deployment process on Vercel. The platform takes care of building and optimizing your app for peak performance.
- **Deployment Monitoring**: Vercel offers tools to monitor your deployment status, letting you view real-time logs and address any issues that might arise.
- **Launch**: Once deployment is successfully completed, "OKR Genius" will be accessible online, offering users a fast and secure experience thanks to Vercel's global infrastructure.

By following these steps, we ensure "OKR Genius" is deployed efficiently, securely, and performs at its best.
