# 26W_CST8915_Lab2-Submission

<ul>
<li>Student Name: Thomas de Haan Carriere</li>
<li>Student ID: 41276876</li>
<li>Course: CST8915 Full-stack Cloud-native Development</li>
<li>Semester: Winter 2026</li>
</ul>

<ul>
<li>Store-Front Repo: https://github.com/thomas7carriere/26W_CST8915_Lab2_Store_Front</li>
<li>Order-Service Repo: https://github.com/thomas7carriere/26W_CST8915_Lab2_Order_Service</li>
<li>Product-Service Repo: https://github.com/thomas7carriere/26W_CST8915_Lab2_Product_Service</li>
</ul>
## Demo Video

🎥 [Watch Demo Video](https://youtu.be/oHgaBzTBJe0)

---
Question: What changes did you make to the order-service and product-service to comply with the Configurations and Backing Services factors of the 12-Factor App methodology?

Answer: .env files were created for both the order-service and product-service. These files contain environment variables for the services. Hard-coded information was replaced with references to the environment variables in the codebase. This allows for config-driven swapping, whereby configurations can be updated in a single file (Backing Services, Factor #4). This approach separates code from configuration (Configuration, Factor #3). The .env files were added to .gitignore, as they can contain sensitive information such as RabbitMQ user details.

Question: Why is it important to use environment variables instead of hard-coding configurations in your application?

Answer: Using environment variables allows configuration changes to take place in a single file, rather than searching through the codebase for hard-coded instances of configuration data. Hard-coding configuration data also poses a security risk if projects are published to a public repository, as sensitive data (e.g., usernames, passwords, API keys) would be visible. Using environment variables and adding them to .gitignore prevents them from being committed, helping mitigate this security risk.

Question: Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?

Answer: In a microservice architecture, each service should be isolated into its own project for several reasons. This allows each service to be independently managed and developed by small teams, rather than having every team work from a single repository. Another benefit is scalability, as the load on each microservice can vary. This allows each service to scale independently based on traffic. With a monolithic approach (having all services in the same application), the entire application would need to scale together, leading to unnecessary costs and wasted resources.
