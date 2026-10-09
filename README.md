# Headquarters ↔ Branch Office Network (Cisco Packet Tracer)

A secure **two-site enterprise network** designed and simulated in **Cisco Packet Tracer**: a headquarters in Tirana and a new branch office in Elbasan, linked by a **site-to-site IPsec VPN**, with each department on its own subnet.

> **Brief:** *You have just been employed by an international company as an IT security engineer. They have built a remote site in another city and want to integrate its network into the system. Design and implement the new network and redesign the old one, taking security procedures into account, with a secure and logical partition for the existing and new departments.*

![Topology](https://user-images.githubusercontent.com/55946528/87252343-8848a700-c472-11ea-92b1-8d91b2762ce4.png)

## What the design covers

- **Two sites**: Headquarters (Tirana) and Branch Office (Elbasan), each with its own edge router, joined over a simulated WAN/cloud through a secure router
- **VLSM addressing**: the HQ `192.168.1.0/24` block is split into right-sized subnets per department (Financial, Administrative, IT, Secretary, CEO, and others), and the branch gets its own subnets for IT, Financial and Administrative
- **Department segmentation**: each department is its own logical network, so traffic and access can be controlled between them
- **Site-to-site IPsec VPN** between HQ and the branch (ISAKMP policy, pre-shared key, ESP transform set and an ACL that defines the traffic to encrypt)
- **SSH-only remote management** for the routers, with local user accounts on routers and switches
- **Physical workspace** that places the buildings on a real map of Tirana and Elbasan
- End-to-end connectivity checked with ICMP in simulation mode: departments at HQ and the branch can all reach each other

## Files

| File | Description |
| --- | --- |
| `Computer Networks_Project_Rexhino_Kovaci.pkt` | The Packet Tracer project (topology, device configs, physical workspace) |

## Opening the project

1. Install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) (built with 7.3; newer versions open it too).
2. Open `Computer Networks_Project_Rexhino_Kovaci.pkt`.
3. Switch between the **Logical** and **Physical** workspaces, or use **Simulation** mode to follow packets across the VPN.

## Screenshots

![Physical workspace – branch office in Elbasan](https://user-images.githubusercontent.com/55946528/87252435-4ec46b80-c473-11ea-89e5-3dd9b33cbf5a.jpg)
![Screenshot](https://user-images.githubusercontent.com/55946528/87252437-508e2f00-c473-11ea-9cf0-e0c3b14ed62c.jpg)
![Screenshot](https://user-images.githubusercontent.com/55946528/87252438-5257f280-c473-11ea-88e0-006a86536b1f.jpg)
![Screenshot](https://user-images.githubusercontent.com/55946528/87252440-5421b600-c473-11ea-8a96-cc0c21a4da81.jpg)
![Screenshot](https://user-images.githubusercontent.com/55946528/87252442-55eb7980-c473-11ea-942c-d9d5b42f0cbc.jpg)

> Note: this is a reworked version of a university networking project. The schema, topology, IP plan, names and colors all differ from the original coursework submission.

---

Built by [Rexhino Kovaci](https://github.com/rexhinokovaci) — DevOps & AI engineer in Tirana, Albania. Need an app built? [Get in touch](mailto:kovacirexhino@gmail.com).
