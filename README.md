# Docker

Interview quetions
Question: what are real-time challanges with docker?
Ans. Docker has a single point of failure. If docker daemon goes down, application is down. 
- docker run as root user which is a security threat.
- resource constraints - if you are running too many containers on a single host, you may experience resource constraints. This can lead to slow performance or crashes.

Solution is podman. Which solves your docker problem. It is not single point failure, it can run as normal non-root user.

Ques. What steps you will take to secure containers?
Ans. 
1. Use distroless or image with not too many packages as your final image in multi stage build.
2. Ensure that networking is configured properly. If required configure custom bridge network and assign them to isolate networks. Create different bridge network for finance application.
3. Use utilities like Sync to scan your container images. Before you push them to production or staging environment.
