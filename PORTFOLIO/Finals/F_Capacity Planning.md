![image](https://github.com/user-attachments/assets/f4392bf5-88f0-4905-bd41-172f94a834f0)


# SYSADM1 -- Capacity Management & Planning

## Part 1. A Simulated Dataset for Capacity Planning Exercise {#part-1.-a-simulated-dataset-for-capacity-planning-exercise .list-paragraph}

![image](https://github.com/user-attachments/assets/0feb28e8-f6a1-48d5-8eca-bcb7aa04393b)

**Scenario:** A mid-sized e-commerce
website is expecting a significant surge in traffic due to an upcoming
holiday sale.

### [Projected Traffic Increase]{.underline}

-   **Expected Peak Traffic:** 5x the normal peak traffic

-   **Peak Time:** 12:00 PM - 3:00 PM on the sale day

### [System Specifications]{.underline}

-   **Server Count:** 5

-   **CPU Cores per Server:** 8

-   **RAM per Server:** 32GB

-   **Network Bandwidth per Server:** 1Gbps

### [Additional Considerations]{.underline}

-   **New Product Launch:** A highly anticipated product will be
    released during the sale.

-   **Marketing Campaign:** A major marketing campaign will be launched
    to promote the sale.

-   **Potential Cyber Threats:** Increased traffic can attract malicious
    actors.

Tasks:

1.  Review the provided server performance data and identify potential
    bottlenecks.

**CPU Usage**: At 9:00 AM, the CPU is only 25% used, but by 3:00 PM,
it's already at 70%. If traffic increases by 5x, the CPU usage will
likely exceed 100%, causing servers to slow down or crash.

**Memory Usage**: Memory usage also rises from 50% at 9:00 AM to 70% at
3:00 PM. A huge increase in users will likely push memory usage to its
limit, making the system unstable or unresponsive.

**Bandwidth Usage**: At 3:00 PM, the servers are handling 200 Mbps in
and 100 Mbps out, which is still within the 1 Gbps limit. However, with
5x traffic, this will easily exceed the limit, leading to slow loading
times or failed connections.

**Response Time**: The response time starts at 200 ms in the morning but
increases to 300 ms by 3:00 PM. This shows the servers are already
struggling with higher traffic. During the sale, the response time could
increase even more, frustrating customers and causing them to leave the
site.

**Cybersecurity Risks**: High traffic can attract hackers or malicious
attacks like DDoS. If we don't prepare for this, the website could go
offline during the most critical hours.

Key Bottlenecks:

1.  CPU Usage: The servers may not handle the processing demands of 5x
    traffic.

2.  Memory Limits: Insufficient RAM could cause crashes or slow
    performance.

3.  Bandwidth Saturation: Increased data transfer during peak hours
    could overwhelm the network.

4.  Response Time: Longer delays could hurt user experience and sales.

5.  Cyber Threats: High traffic may attract DDoS attacks or other
    malicious activities, leading to system instability.

**Proposed Solutions**

1.  **Add More Servers**

    -   To handle the extra traffic, we could add more servers to
        increase the total CPU, RAM, and bandwidth available. For
        example, adding two extra servers would boost our overall
        capacity by 40%. This will ensure that the website doesn't crash
        under heavy traffic.

2.  **Upgrade Current Servers**

    -   If adding servers is too expensive, we could upgrade the
        existing ones. For instance, we could replace the CPUs with
        higher-performance models or add more RAM to each server. This
        is a cheaper option than adding servers but may not handle
        traffic as effectively as scaling horizontally.

3.  **Use a Content Delivery Network (CDN)**

    -   A CDN stores copies of static content (like images, CSS, and
        JavaScript) on multiple servers across different locations. When
        users visit the website, they'll download these files from the
        nearest CDN server, which reduces the load on our main servers
        and speeds up the site for users.

4.  **Implement Load Balancers**

    -   Load balancers distribute incoming traffic evenly across all
        servers. This prevents any single server from becoming
        overwhelmed. It also improves response times because user
        requests are directed to the least busy server.

5.  **Strengthen Cybersecurity**

    -   We should install firewalls, set up DDoS protection, and monitor
        traffic in real-time. This will help block malicious traffic and
        protect the website during the sale.

6.  **Perform Stress Testing**

    -   Before the sale, we should simulate a 5x traffic surge to test
        how well the system handles it. This will help us identify and
        fix any weak points in advance.

```{=html}
<!-- -->
```
2.  Discuss the pros and cons of each proposed solution by filling out
    the table below.

**Evaluation of Solutions**

![image](https://github.com/user-attachments/assets/2ba83286-30f0-4171-a52f-24541d56df92)
![image](https://github.com/user-attachments/assets/8dfc68ac-c991-47ab-8509-6a21ce1291e6)



Grading Rubric:
![image](https://github.com/user-attachments/assets/f0bd0117-450c-4e9d-aa72-2af29f6e8787)


**Part 2. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

![image](https://github.com/user-attachments/assets/45a0635a-6cf8-49e7-9d55-4f0678f2f086)


**Potential Bottlenecks:**

-   **Bandwidth Constraints on Uplinks:** The uplinks connecting Layer 2
    switches to the Core Switch or the Core Switch to the Edge Router
    might not have sufficient bandwidth, especially if they are using
    older technologies like 1 Gbps Ethernet, limiting the overall
    throughput and causing delays during peak traffic.

-   **Lack of Redundancy:** The network lacks redundant links between
    critical components such as routers, switches, and servers. A single
    point of failure, such as a broken link or hardware malfunction,
    could lead to significant downtime and service disruption.

-   **Scalability Limits:** As user demand grows, the current
    architecture may not support adding more devices or servers without
    significant reconfiguration. Limited capacity in the current switch
    model could also restrict the ability to scale VLANs or handle
    additional traffic efficiently.

-   **Inter-VLAN Traffic Congestion:** High inter-VLAN traffic would
    rely heavily on the Core Switch for routing, increasing its load and
    reducing performance. This issue can become particularly problematic
    if applications or services in different VLANs communicate
    frequently.

-   **Security Vulnerabilities (No Firewalls)**:

Without firewalls, the network is directly exposed to external threats
through edge routers. The lack of traffic filtering or inspection
creates the following risks:

1.  **External Attacks**: Vulnerability to unauthorized access, malware,
    and DDoS attacks.

2.  **Internal Threats**: Devices within one VLAN can potentially
    compromise devices in other VLANs if ACLs and VLAN isolation are not
    effectively configured.

3.  **Unrestricted Traffic**: Inbound and outbound traffic are not
    thoroughly inspected, allowing malicious packets to traverse the
    network undetected.

-   **Security Processing Delays:** Increased security processing for
    monitoring and filtering traffic in a high-demand environment can
    slow down packet forwarding and response times if security measures
    like intrusion detection/prevention systems are not scaled
    appropriately. The absence of firewalls places a greater burden on
    edge routers to handle basic security tasks like ACLs and intrusion
    detection. If these systems are not scaled appropriately, they can
    slow down packet forwarding and response times.

**SOLUTION:**

To improve the scalability and performance of the network, several
strategies are recommended, focusing on both hardware enhancements and
software configurations. First, the deployment of dual edge routers
connected to Converge and PLDT ISPs with failover capabilities ensures
reliable internet connectivity. This setup minimizes the risk of
downtime by providing load balancing and redundancy, effectively
addressing potential failures. The existing Layer 3 core switch will
remain central to the network, handling inter-VLAN routing efficiently
without the need for upgrading the Layer 2 access switches. To further
enhance network performance, high-speed 10Gbps uplinks should be
implemented between the core switch and both the edge routers and the
Layer 2 access switches. These uplinks will accommodate increased
traffic volumes, reducing congestion and ensuring faster data transfers,
especially during peak periods.

Load balancing is crucial for VLAN 1, where multiple servers handle user
requests. Installing load balancers will distribute traffic evenly among
the servers, preventing overload and improving response times. Security
is also a priority, and the addition of redundant firewalls between the
edge routers and the core switch will protect the network from external
threats. Also, VLAN isolation and the implementation of Access Control
Lists (ACLs) on the Layer 3 core switch will safeguard sensitive
resources and restrict unauthorized access. To proactively monitor and
manage network performance, integrating tools like SNMP will enable
real-time tracking, allowing IT personnel to identify and address
potential bottlenecks promptly.

While these strategies significantly improve scalability, reliability,
and performance, they also present challenges. Upgrades such as 10Gbps
uplinks, load balancers, and firewalls involve considerable costs, which
may affect limited budgets. Additionally, the increased complexity of
managing redundant systems, load balancers, and monitoring tools
requires skilled IT staff to ensure smooth operations. Despite these
challenges, this proposed design effectively prepares the network for
future growth and peak traffic demands while maintaining a secure and
reliable infrastructure.

> **Proposed Network Design**

![image](https://github.com/user-attachments/assets/6ce792a8-f6f7-4873-8941-4b506329ab8d)


  ------------------------------------------------------------------------------
![image](https://github.com/user-attachments/assets/a58e499f-464e-41c5-baad-fcabd05e8213)

