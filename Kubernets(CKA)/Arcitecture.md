
1. KeyCloak
2. Velero
3. When you run kubectl apply command what happens in the background?
4. How can we take backup of our etcd?
5. By default can we run components on master plane it has taint and toleration?
6. What Does `usermod` Do?
7. How you can give access you deployment to the any service running on aws.(using addon)
8. EKS Pod Identity and IRSA
9. Metrics Server
10. kubeflow
11. ho pv and pvc behave across zones in eks or general kubernetes?
12. What is a Pod Disruption Budget (PDB)?
13. If you want two pods per node (instead of the one-per-node model that a DaemonSet enforces), a DaemonSet won’t work because it’s strictly 1 pod per node.
14. what are challenges sheduling pods multi node, multi az setup




#### KeyCloak

![[Pasted image 20250620170644.png]]


![[Pasted image 20250620170919.png]]


## What is **Keycloak**?

**Keycloak** is an **open-source identity and access management tool**. It helps you **manage users**, **logins**, and **permissions** in your applications — **without writing your own authentication system**.

---

## 💡 Easy Way to Understand:

Imagine you're building a website or app. You want users to:

- 🔐 Log in with username and password
    
- 📧 Sign up or reset their password
    
- 👥 Use Google, Facebook, GitHub, etc. to log in
    
- 🧑‍⚖️ Have different roles like admin, editor, viewer
    
- 🔁 Stay logged in securely
    

➡️ Instead of building all this yourself, you use **Keycloak**.


If we do not want to attach default service account to our pod.

![[Pasted image 20250529202308.png]]



## Which Database Does `etcd` Use Internally?

**`etcd` uses boltdb — specifically a fork called **`bbolt`**, which is a low-level **embedded key-value database** written in **Go**.

---

## ⚙️ What is `bbolt`?

- `bbolt` is a **B+Tree-based**, file-backed **key-value store**
    
- Everything is stored inside a **single `.db` file** on disk
    
- Transactions are **ACID compliant** (Atomic, Consistent, Isolated, Durable)
    

Think of it like **SQLite for key-value data** — no server, no client, just a file.




