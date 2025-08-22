Perfect 👍 Let’s do this step by step in English, very clear and systematic:


---

🚀 How to Create an Ubuntu Virtual Machine (EC2) on AWS Free Tier and Install Nginx


---

Step 1: Create AWS Account

Go to AWS Free Tier.

Sign up for a free account.

You will get 750 hours per month of t2.micro instance free for 12 months.



---

Step 2: Launch an EC2 Instance (Ubuntu VM)

1. Go to AWS Management Console.


2. Navigate to Services → EC2 → Launch Instance.


3. Give your instance a name (e.g., my-ubuntu-server).


4. Choose OS → Ubuntu Server 22.04 LTS (Free tier eligible).


5. Choose Instance Type → t2.micro (Free tier eligible).


6. Create a new Key Pair (download the .pem file, e.g., mykey.pem).

This is required to connect to your server via SSH.



7. Configure Security Group → Add inbound rules:

SSH (Port 22) → Your IP.

HTTP (Port 80) → Anywhere (so people can see your website).

(Optional: HTTPS (Port 443) for SSL).



8. Click Launch Instance.




---

Step 3: Connect to EC2 Instance

1. Open your terminal.


2. Set correct permissions for the .pem key file:

chmod 400 mykey.pem


3. Connect via SSH:

ssh -i mykey.pem ubuntu@<EC2-Public-IP>

Replace <EC2-Public-IP> with the public IP shown in your EC2 dashboard.





---

Step 4: Update the Server

sudo apt update && sudo apt upgrade -y


---

Step 5: Install Nginx

1. Install Nginx:

sudo apt install nginx -y


2. Start and enable the service:

sudo systemctl start nginx
sudo systemctl enable nginx




---

Step 6: Test Nginx

Open your browser and visit:

http://<EC2-Public-IP>

You should see the Nginx default welcome page ✅



---

Step 7 (Optional): Host Your Own Website

Default Nginx root folder:

/var/www/html

Replace index.html with your own file. Example:

echo "<h1>Hello from My AWS Ubuntu Server 🚀</h1>" | sudo tee /var/www/html/index.html

Refresh your browser → You’ll see your custom page.



---

✅ Now your Ubuntu VM on AWS Free Tier is running with Nginx web server.


---

Do you also want me to show you the same steps with a simple diagram/flowchart (AWS → EC2 → Public IP → Nginx → Browser) so you can visualize the process?

