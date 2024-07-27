# Features

#### Elastic Load Balancing (ELB) Detailed Concepts with Example Scenarios

**1. Application Load Balancer (ALB)**

* **Layer 7 Load Balancer**: Operates at the application layer (HTTP/HTTPS).

**Features and Example Scenarios**:

1. **Path-based Routing**
   * **Feature**: Routes traffic to different target groups based on the URL path.
   * **Scenario**: You have a website with multiple microservices, e.g., `/api` for backend services and `/images` for serving static images. Configure ALB to route requests to different target groups based on these paths.
2. **Host-based Routing**
   * **Feature**: Routes traffic based on the hostname in the request.
   * **Scenario**: You have multiple domains, `example.com` and `example.org`, pointing to different applications. Use ALB to route traffic based on the `Host` header, sending requests for `example.com` to one target group and `example.org` to another.
3. **HTTP/2 and WebSocket Support**
   * **Feature**: Supports HTTP/2 and WebSocket protocols for improved performance and real-time communication.
   * **Scenario**: A chat application requires real-time communication. Configure ALB to support WebSocket connections for seamless communication between clients and servers.
4. **SSL Termination**
   * **Feature**: Offloads SSL decryption/encryption to the load balancer.
   * **Scenario**: Offload SSL termination to ALB to reduce the load on your backend servers. Use AWS Certificate Manager (ACM) to manage SSL certificates.
5. **Integration with AWS WAF**
   * **Feature**: Protects applications from common web exploits by integrating with AWS WAF.
   * **Scenario**: A public-facing web application needs protection against SQL injection and cross-site scripting (XSS) attacks. Integrate ALB with AWS WAF to apply security rules.
6. **Sticky Sessions**
   * **Feature**: Ensures a user’s session is consistently routed to the same target.
   * **Scenario**: An e-commerce website maintains user session data. Enable sticky sessions on ALB to ensure users' shopping carts are consistent during their visits.
7. **Content-based Routing**
   * **Feature**: Routes traffic based on the content of the request.
   * **Scenario**: Different versions of an application are deployed. Route requests containing `beta` in the URL to the beta version and other requests to the stable version.
8. **Redirects and Fixed Responses**
   * **Feature**: Configures HTTP redirects or fixed responses.
   * **Scenario**: Redirect HTTP traffic to HTTPS. Set up ALB rules to redirect all `http://` requests to `https://`.
9. **Monitoring via CloudWatch Metrics**
   * **Feature**: Provides metrics for monitoring the load balancer.
   * **Scenario**: Use CloudWatch metrics to monitor request count, latency, and target health. Set up alarms to notify when latency exceeds a certain threshold.

**2. Network Load Balancer (NLB)**

* **Layer 4 Load Balancer**: Operates at the transport layer (TCP/UDP).

**Features and Example Scenarios**:

1. **Handles Millions of Requests per Second**
   * **Feature**: Supports high traffic loads with low latencies.
   * **Scenario**: A financial trading application requires handling millions of transactions per second with low latency. Use NLB for its high throughput capabilities.
2. **Low Latencies**
   * **Feature**: Provides ultra-low latency load balancing.
   * **Scenario**: Real-time gaming applications need minimal latency. NLB ensures fast response times for game state updates.
3. **Static IP Addresses and Elastic IP Support**
   * **Feature**: Assigns static IPs or Elastic IPs to the load balancer.
   * **Scenario**: An on-premises system integrates with AWS services via a VPN. Use static IPs with NLB to allow consistent IP whitelisting.
4. **TLS Offloading**
   * **Feature**: Offloads TLS decryption/encryption to the load balancer.
   * **Scenario**: Offload TLS termination to NLB for services that require high performance, such as IoT data ingestion endpoints.
5. **Preserve Client IP**
   * **Feature**: Maintains the client’s IP address for backend servers.
   * **Scenario**: A logging service needs the original client IP for accurate logging and auditing. NLB preserves client IPs for this purpose.
6. **Health Checks for Targets**
   * **Feature**: Regularly checks the health of registered targets.
   * **Scenario**: Use TCP or HTTP health checks to ensure backend database servers are healthy and can handle requests.

**3. Classic Load Balancer (CLB)**

* **Legacy Load Balancer**: Supports both HTTP/HTTPS and TCP/SSL.

**Features and Example Scenarios**:

1. **Basic Load Balancing Across Multiple EC2 Instances**
   * **Feature**: Distributes incoming traffic across multiple EC2 instances.
   * **Scenario**: A legacy application requires simple load balancing without advanced routing rules. CLB distributes traffic evenly across the instances.
2. **Supports Both Layer 4 and Layer 7**
   * **Feature**: Can handle both TCP/SSL (Layer 4) and HTTP/HTTPS (Layer 7) traffic.
   * **Scenario**: A mixed-traffic application needs to load balance both HTTP requests and TCP connections. CLB can manage both types of traffic.
3. **Sticky Sessions**
   * **Feature**: Ensures a user’s session is consistently routed to the same target.
   * **Scenario**: An online banking application requires maintaining session consistency. Enable sticky sessions on CLB to ensure users remain connected to the same instance.
4. **SSL Termination**
   * **Feature**: Offloads SSL decryption/encryption to the load balancer.
   * **Scenario**: Offload SSL termination to CLB to reduce the computational load on backend servers. Use SSL certificates managed in ACM.

#### Summary Table

<table data-full-width="true"><thead><tr><th>Feature</th><th>ALB</th><th>NLB</th><th>CLB</th></tr></thead><tbody><tr><td>Layer</td><td>7 (HTTP/HTTPS)</td><td>4 (TCP/UDP)</td><td>4 (TCP/SSL) and 7 (HTTP/HTTPS)</td></tr><tr><td>Path-based Routing</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>Host-based Routing</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>HTTP/2 and WebSocket Support</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>SSL Termination</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>AWS WAF Integration</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>Sticky Sessions</td><td>Yes</td><td>No</td><td>Yes</td></tr><tr><td>Content-based Routing</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>Redirects and Fixed Responses</td><td>Yes</td><td>No</td><td>No</td></tr><tr><td>CloudWatch Metrics</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>Handles Millions of Requests</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>Low Latencies</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>Static IPs/Elastic IPs</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>Preserve Client IP</td><td>No</td><td>Yes</td><td>No</td></tr><tr><td>Health Checks</td><td>Yes</td><td>Yes</td><td>Yes</td></tr></tbody></table>

These examples and features provide a comprehensive understanding of how different types of AWS Load Balancers can be utilized to address specific application requirements and scenarios. This knowledge is crucial for both practical applications and preparation for the AWS Solution Architect Professional exam.
