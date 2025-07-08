# Cloud_computing_Minor-major_project_Myself

AWS S3 Static Website Hosting – College Admission Form

I created S3 Bucket!![image](https://github.com/user-attachments/assets/51c42efa-2e91-4c27-b3d7-fbd0662db661)
Create a simple HTML file named index.html. ![image](https://github.com/user-attachments/assets/7193cb6d-9afa-4b52-b2f2-45a1a58d41cd)
Successfully given the bucket policy ![image](https://github.com/user-attachments/assets/fdd48193-2326-40a4-9a18-b9fc67645e25)
Tried using the public URL for the object i created inn index.html got that ![image](https://github.com/user-attachments/assets/5854d442-dbad-46f2-a097-a078fb8defdf)


-----
 How to Start Explaining Your Project
“In my minor project, I created a college admission form and hosted it as a static website using AWS S3. I handled bucket creation, file deployment, public access permissions using bucket policy, and enabled static website hosting. The site was accessible through a public endpoint.”

🎯 Expected Interview Questions + Sample Answers
1. What is Amazon S3 and why did you use it?
Answer:
Amazon S3 (Simple Storage Service) is an object storage service. I used it because it's cost-effective and easy to use for hosting static websites like HTML/CSS files.

2. What is static website hosting in S3?
Answer:
Static website hosting allows you to serve static content (HTML, CSS, JS) directly from an S3 bucket using a website endpoint. You just upload your files and S3 delivers them over HTTP.

3. Why did you need to make the bucket objects public?
Answer:
By default, S3 blocks public access for security reasons. Since I wanted my website to be publicly accessible via the web, I had to make the files (like index.html) public using a bucket policy.

4. What policy did you use to allow public access?
Answer:
I used a bucket policy that allowed s3:GetObject permission for everyone ("Principal": "*"). Here's a short version of the policy:

json
Copy
Edit
{
  "Effect": "Allow",
  "Principal": "*",
  "Action": "s3:GetObject",
  "Resource": "arn:aws:s3:::mybucky123/*"
}
This makes every object in the bucket readable by anyone.

5. What are some security concerns with making a bucket public?
Answer:
Making buckets public can expose sensitive data. Anyone with the link can access the files. That’s why AWS blocks public access by default. It's important to only do it for safe content like static web pages.

6. Can you use S3 for dynamic websites?
Answer:
No, S3 only supports static websites. It can't process backend logic like PHP or databases. For dynamic websites, we’d need services like EC2, Lambda, or Elastic Beanstalk.

7. What are the alternatives to S3 for static hosting?
Answer:

GitHub Pages

Netlify

Firebase Hosting

AWS Amplify (also built on S3 internally)

8. How is S3 different from EC2 for hosting?
Answer:

S3 is for static websites — no backend processing

EC2 is a virtual server — supports full web servers (Apache, Nginx), dynamic apps, and databases

9. What is the difference between bucket policy and ACL?
Answer:

ACL (Access Control List): Object-level access, limited control

Bucket Policy: JSON-based, more flexible, works at bucket or object level
AWS recommends using bucket policies for public access today.

10. What happens if the index.html file is missing?
Answer:
The website endpoint will give a 403 or 404 error since it cannot find the root document specified in the static website hosting settings.

🧠 Bonus Tips to Impress:
Mention you disabled Block Public Access before applying the bucket policy.

Say you tested the endpoint using a browser to ensure the form loaded correctly.

Optional: Mention how you could improve it (e.g., add CSS or connect it to a backend later with Lambda/API Gateway).

“As part of my minor project, I built and hosted a College Admission Form using Amazon S3's static website hosting feature. I started by creating a bucket named mybucky123, then uploaded an index.html file that contained a basic HTML form for student details like name, age, and course selection.

I configured the bucket to disable the default public access block, and then applied a bucket policy that allowed s3:GetObject for all users, enabling the website to be publicly accessible. After that, I enabled static website hosting by setting index.html as the main document.

Finally, I tested the website using the S3 static hosting endpoint URL to make sure it loaded properly in the browser. This project helped me understand key AWS concepts like S3, bucket policies, access permissions, and static hosting in real-world scenarios.”

