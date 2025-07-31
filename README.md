# S3 Web Application Deployment

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![SonarQube](https://img.shields.io/badge/SonarQube-black?style=for-the-badge&logo=sonarqube&logoColor=4E9BCD)

## DevOps Pipeline

Automated CI/CD pipeline for deploying static web applications to AWS S3 with CloudFront distribution.

### Architecture
- **S3 Static Website Hosting** - Cost-effective static content delivery
- **CloudFront CDN** - Global content distribution and caching
- **GitHub Actions** - Automated deployment pipeline
- **SonarQube** - Code quality and security analysis

### Pipeline Workflow
1. **Code Quality Check** - SonarQube static analysis
2. **AWS Deployment** - S3 sync with file exclusions
3. **Cache Invalidation** - CloudFront distribution refresh

### Required Secrets
```
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_REGION
S3_BUCKET_NAME
CLOUDFRONT_DISTRIBUTION_ID
SONAR_TOKEN
```

### Deployment Triggers
- **Push to main** - Deploys when web files (HTML, CSS, JS, images, fonts) change
- **Pull requests** - Validates code quality before merge
- **Manual dispatch** - On-demand deployment capability