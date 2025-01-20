Host a Static Website in AWS

This project demonstrates how to host a static website using AWS services: S3, Route 53, Certificate Manager, and CloudFront. By following this guide, you'll create a scalable, secure, and globally distributed website.

 Prerequisites

- An AWS account.
- A registered domain (can be purchased through Route 53 or another domain registrar).
- Basic knowledge of AWS services.

 Steps

 1. Create and Configure an S3 Bucket
   - Navigate to the S3 console and create a bucket.
   - Enable Static Website Hosting in the bucket properties.
   - Upload your static website files to the bucket.
   - Set the bucket policy to allow public read access (if applicable).

 2. Set Up Route 53
   - Create a hosted zone in Route 53 for your domain.
   - Update your domain's Name Servers (NS) with the values provided by Route 53 (if using a third-party registrar).

 3. Generate an SSL Certificate
   - Use AWS Certificate Manager to request a public certificate for your domain.
   - Validate the certificate using DNS validation through Route 53.

 4. Create a CloudFront Distribution
   - Use the CloudFront console to create a distribution for your S3 bucket.
   - Attach the SSL certificate from AWS Certificate Manager.
   - Configure a custom origin for your S3 bucket (ensure the bucket is not publicly accessible, and enable OAI for secure access).
   - Configure the custom domain name and default root object.

 5. Update DNS Records in Route 53
   - Create an A record (Alias) pointing to the CloudFront distribution in your hosted zone.
   - Test the domain to ensure it resolves to your website.

 Features

- Scalable Hosting: Using S3 for hosting your static website.
- Custom Domain: Easily configure custom domains with Route 53.
- SSL Security: Provide HTTPS access with AWS Certificate Manager.
- Content Distribution: Leverage CloudFront for faster content delivery across the globe.

 Resources
- [Amazon S3 Documentation](https://docs.aws.amazon.com/s3/index.html)
- [Amazon Route 53 Documentation](https://docs.aws.amazon.com/route53/)
- [AWS Certificate Manager Documentation](https://docs.aws.amazon.com/acm/)
- [Amazon CloudFront Documentation](https://docs.aws.amazon.com/cloudfront/)
