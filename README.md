# What is Nutanix AOS?

**AOS (Acropolis Operating System)** is the software that runs on servers to create **Hyperconverged Infrastructure (HCI)**.  
It combines **compute, storage, and networking** into one system.  
Instead of needing separate **SAN/NAS storage**, AOS turns all the servers' disks into **one shared pool of storage**.

## How Does It Work?
Think of a **traditional data center**:  
❌ You need separate **servers (compute)**, **storage (SAN)**, and **networking**.  
✅ **With Nutanix AOS, everything is combined into one HCI system.**

1️⃣ You install **AOS on x86 servers** (Dell, Lenovo, HPE, etc.).  
2️⃣ Each server (node) contributes **CPU, RAM, and local disks**.  
3️⃣ AOS **pools all disks together** → No need for separate storage (SAN/NAS).  
4️⃣ You can **run virtual machines (VMs) on top of it**.  
5️⃣ **As you add more servers (nodes), AOS dynamically expands storage and compute resources, ensuring scalability without downtime.**

---

## Key Parts of AOS

### 1️⃣ Virtualization (Compute) → **Nutanix AHV**
- Runs **virtual machines (VMs)** using Nutanix **AHV (free hypervisor)** or **VMware ESXi**.  
- **AHV is the default hypervisor, but customers can also choose VMware ESXi if needed.**  

### 2️⃣ Storage (Software-Defined Storage - SDS) → **Nutanix DSF** (Similar to IBM Storage Virtualize)
- AOS combines **all disks into one shared storage pool** for VMs.  
- **DSF eliminates the need for separate SAN/NAS**, providing **enterprise-class storage with built-in redundancy and high availability.**  

### 3️⃣ Management → **Prism UI**
- A single **web-based UI** to manage **VMs, storage, and networking**.  
- **Easier than VMware vCenter.**  

---

## Nutanix AOS vs. Traditional Infrastructure

| **Function**     | **Nutanix Component**           | **Replaces**                  |
|----------------|----------------------------------|--------------------------------|
| **Virtualization**  | AHV (Acropolis Hypervisor)       | VMware vSphere, Hyper-V        |
| **Storage**        | DSF (Distributed Storage Fabric) | Traditional SAN/NAS (NetApp, Dell EMC) |
| **Management**     | Prism UI                         | VMware vCenter, Storage Manager |

---

## 🔹 How Nutanix AOS Works in a Data Center
1️⃣ You have multiple **x86 servers** (from Dell, Lenovo, HPE, Supermicro, etc.).  
2️⃣ Each server has its own **local disks** (SSD, HDD, or NVMe).  
3️⃣ You **install Nutanix AOS** on each server.  
4️⃣ AOS **automatically combines all storage** into a **single storage pool** (using DSF – Distributed Storage Fabric).  
5️⃣ You manage everything (**compute + storage + networking**) through **Prism UI**.  
6️⃣ You can **create and run VMs on any server** in the cluster.  
7️⃣ **As you add more servers, the system automatically expands** (both storage and compute) **without disruption**.  

💡 **This eliminates the need for external SAN/NAS storage**—AOS makes all local disks act as **one shared, distributed storage system**.

---

## What Happens When You Install AOS?
When you install **AOS on an x86 server**, it **automatically sets up** the core Nutanix components:

| **Component**                     | **Installed Automatically?** | **Purpose** |
|----------------------------------|-------------------------|-----------------------------------------------|
| **DSF (Distributed Storage Fabric)**  | ✅ Yes                   | Creates a **single storage pool** across all servers (No SAN needed). |
| **Prism UI**                          | ✅ Yes                   | Manages everything (**compute, storage, networking**) from one interface. |
| **AHV (Acropolis Hypervisor)**        | ✅ Yes (by default)      | Runs **virtual machines (VMs)** (Alternative to VMware vSphere). |

---

## 🚀 Steps to Deploy Nutanix AOS
1️⃣ **Install AOS on each x86 server.**  
2️⃣ AOS **automatically sets up DSF** (turns all disks into shared storage).  
3️⃣ AOS **installs Prism** for management.  
4️⃣ AOS **installs AHV** (unless you select VMware ESXi).  
5️⃣ **Cluster is ready** → **You can create VMs immediately!**  

---

## 🔹 Why Nutanix AOS?
✅ **Built-in compute (AHV), storage (DSF), and management (Prism).**  
✅ **No need for external storage—DSF eliminates SAN/NAS dependency.**  
✅ **Simplifies IT operations with an easy-to-use UI (Prism).**  
✅ **Scales effortlessly—just add more nodes!**  
✅ **Reduces costs compared to traditional VMware setups.**  

💡 **By combining compute, storage, and management into a single platform, Nutanix AOS simplifies IT, reduces costs, and eliminates the complexity of traditional infrastructure.**

💡 Installing AOS turns your x86 servers into a full HCI appliance.
---
