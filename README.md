Here is the English translation for the Chinese text in your provided document:

---

## Project Introduction  

Based on LQ's chat2api project, build a shared platform for easy access by your friends.  
Project address: [https://github.com/lanqian528/chat2api](https://github.com/lanqian528/chat2api)

It also supports Qin Shi Huang's fuclaude. If an open-source claude image is available in the future, it will be prioritized for adaptation to open source.

## Configuration Items  
In the `docker-compose.yml`, configure the following three environment variables:

```
secret_key should be complex.  
authorization should match the value of the `authorization` environment variable in chat2api.  
domain_chatgpt is the site address of chat2api, which needs to be replaced with your own project address.
```

### Direct Deployment

```bash
git clone https://github.com/h88782481/chat-share
cd chat-share
pip install -r requirements.txt
python app.py
```

### Docker Deployment

You need to install Docker and Docker Compose.

```bash
docker run -d \
  --name chat-share \
  -p 5100:5100 \
  -e SECRET_KEY=your_admin_secret_key \
  -e AUTHORIZATION=your_authorization \
  -e DOMAIN_CHATGPT=http://127.0.0.1:5005 \
  ghcr.io/h88782481/chat-share:latest
```

### (Recommended) Docker Compose Deployment

Create a new directory, such as `chat-share`, and enter the directory:

```bash
mkdir chat-share
cd chat-share
```

Download the `docker-compose.yml` file from the repository into this directory:

```bash
wget https://raw.githubusercontent.com/h88782481/Chat-Share/main/docker-compose.yml
```

Modify the environment variables in the `docker-compose-warp.yml` file, save, and then run:

```bash
docker-compose up -d
```

## Page Preview  

### Login Page  
Default admin account:
```
Username: admin
Password: password
```
Please log in and change the username and password in the user management section. 

![image](https://github.com/user-attachments/assets/2541f8d0-eb76-42fb-8ec7-24199fc93372)

### Backend Management Page

![image](https://github.com/user-attachments/assets/56ea9c43-6cfc-418c-a461-d4fc35b354eb)

## License

MIT License

---

Let me know if you need further modifications!
