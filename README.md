# aws-photo-doc-storage-repo
Beginner-friendly AWS demo for building a Photo &amp; Document Storage Web App using Amazon Cognito, IAM roles, and S3. Includes static HTML frontend for login, secure file upload, and file listing with per-user isolation.

## **Demo Overview**

Participants will learn to:

1. Deploy a simple front-end using static HTML.
2. Set up an Amazon S3 bucket for secure file storage.
3. Configure authentication using Amazon Cognito.
4. Use IAM roles to securely upload and retrieve files through the web interface.

**Services Used:**

| Service | Purpose |
|---------|---------|
| Amazon Cognito | User authentication and issuance of temporary AWS credentials |
| IAM Role | Restricts users to their **private folder** in S3 |
| Amazon S3 | Stores user-uploaded photos and documents securely |
| Static HTML / JS | Frontend interface for login, file upload, and listing files |

---

## **Files in this Repository**

| File | Purpose |
|------|---------|
| `index.html` | Main app page: login/logout, file upload, and file listing |
| `logout.html` | Logs out users securely via Cognito Hosted UI |
| `logout-redirect.html` | Post-logout page with login button |
| `cors.json` | CORS configuration for S3 bucket |

---

## **Placeholders to Replace**

Before running the demo, update these placeholders in the HTML files:

1. **Cognito, Amplify & IAM Configuration**:
   ```js
   // Cognito configuration
   region: "YOUR_AWS_REGION",
   userPoolId: "YOUR_USER_POOL_ID",
   userPoolWebClientId: "YOUR_APP_CLIENT_ID",
   identityPoolId: "YOUR_IDENTITY_POOL_ID",
   YOUR_COGNITO_DOMAIN: "Your Cognito User Pool domain name"
   YOUR_APP_DOMAIN: "The domain where your HTML files are hosted"
   // S3 bucket
   bucketName: "YOUR_S3_BUCKET_NAME",
   region: "YOUR_AWS_REGION"
