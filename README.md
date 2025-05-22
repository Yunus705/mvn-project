# CI/CD Pipeline for Maven Web Application using Jenkins

This project demonstrates a simple CI/CD pipeline setup for a Maven-based Hello World web application. The pipeline includes the following stages:

- **Test**
- **Build**
- **Deploy to Testing Server (Tomcat)**
- **Manual Approval**
- **Deploy to Production Server (Tomcat)**

---

## 🛠 Technologies Used

- Java (JSP/Servlet)
- Maven
- Jenkins
- GitHub
- Apache Tomcat (Testing and Production servers)
- EC2 (AWS)

---

## 🧪 CI/CD Pipeline Stages

1. **Test**: Runs basic unit tests (if any).
2. **Build**: Uses Maven to build the project and create a `.war` file.
3. **Deploy to Testing**: Copies `.war` to `/webapps` of testing Tomcat server using SSH.
4. **Manual Approval**: Jenkins waits for user input before production deployment.
5. **Deploy to Production**: Upon approval, deploys `.war` to production Tomcat server.

---

## 🌐 Live EC2 Servers Setup

- Jenkins Server (for managing pipeline)
- Testing Server (Tomcat)
- Production Server (Tomcat)

---

## ✅ How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/Yunus705/mvn-project.git
   ```
2. Open Jenkins → Create a pipeline → Link your GitHub repo.

3. Make sure SSH keys are set up to access testing and production servers.

4. Run the pipeline and monitor the stages.

---


