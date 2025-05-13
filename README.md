# ecommerce-flask-aws-app
Scalable e-commerce app built with Flask and deployed on AWS using EC2, RDS, S3, ELB, and Auto Scaling.
# 🛒 Scalable E-Commerce Web App on AWS

This project is a **full-stack e-commerce application built with Flask** and deployed on **AWS Cloud Infrastructure** for high availability, performance, and scalability. It uses **EC2** for web hosting, **RDS (MySQL)** for relational database storage, **S3** for file storage, and integrates **Elastic Load Balancer (ELB)** and **Auto Scaling** to handle traffic efficiently.

---

##  Features

- Product listing with images, prices, and descriptions
- Add to cart, checkout simulation
- Image upload and storage on AWS S3
- Backend using Flask and MySQL (via RDS)
- Load-balanced architecture with ELB
- Auto Scaling Group for scalability
- Basic authentication and session handling

---

## Technologies & Services Used

| Category       | Tools & Services                           |
|----------------|--------------------------------------------|
| Frontend       | HTML, CSS, Bootstrap                       |
| Backend        | Python Flask                               |
| Database       | Amazon RDS (MySQL)                         |
| File Storage   | Amazon S3                                  |
| Hosting        | Amazon EC2 (Ubuntu + Apache/Nginx + Gunicorn) |
| Load Balancing | Elastic Load Balancer (ALB)                |
| Scaling        | Auto Scaling Group                         |
| VCS & CI/CD    | Git, GitHub                                |

---

Setup Instructions

### 1.Launch EC2 Instance
- Use Ubuntu 20.04
- Install Python, pip, Git, virtualenv
- Clone the project and set up virtual environment:
  ```bash
  git clone https://github.com/yourusername/ecommerce-flask-app.git
  cd ecommerce-flask-app
  python3 -m venv venv
  source venv/bin/activate
  pip install -r requirements.txt
2. Configure MySQL (RDS)
Create an RDS MySQL instance

Update config.py with the RDS endpoint and credentials

3. Configure S3
Create an S3 bucket

Set proper CORS and bucket policy

Add access keys to .env file or use IAM roles

4. Deploy Flask App
Use Gunicorn + Nginx or Apache for production

Start the app:

bash
Copy
Edit
gunicorn -w 4 app:app

5. Add ELB & Auto Scaling
Place EC2 in an Auto Scaling Group

Attach to Application Load Balancer

Set CPU threshold-based scaling policies

