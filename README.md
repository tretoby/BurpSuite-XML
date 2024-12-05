# **Burp Suite Project: Identifying and Exploiting XXE Vulnerabilities**

## **Task**  
Leverage **Burp Suite** to intercept and analyze web page requests, identify potential XML External Entity (XXE) vulnerabilities, and execute a targeted attack to extract sensitive information from 20 user accounts.

---

## **Steps**

### **1. Launch Burp Suite**  
Begin by starting Burp Suite to initialize the testing environment.  

<img width="586" alt="image" src="https://github.com/user-attachments/assets/d88f99f9-e855-4f99-81b3-3c70f1b437b9">


---

### **2. Access the Proxy Tab**  
Navigate to the **Proxy** tab to enable interception of requests between the browser and the server.  

<img width="604" alt="image" src="https://github.com/user-attachments/assets/59e8fcec-ebf3-4c0c-9229-8378a079a090">


---

### **3. Open the Burp Suite Browser**  
Use the Burp Suite browser to interact with the target web application for testing.  

<img width="602" alt="image" src="https://github.com/user-attachments/assets/62cd4d9a-45e5-4637-ab9f-8b2cd8179007">


---

### **4. Navigate to the Target Webpage**  
Access the webpage through the **Burp Browser**, preparing for analysis and testing.  
<img width="585" alt="image" src="https://github.com/user-attachments/assets/008c6491-0d2a-421c-b545-759643212ce3">


---

### **5. Enable Request Interception**  
Return to the **Proxy** tab and enable **Intercept** to capture HTTP requests.  

<img width="598" alt="image" src="https://github.com/user-attachments/assets/0e566f0b-fdfc-4a7a-aa58-1d079e5f55d3">


---

### **6. Familiarize Yourself with the Proxy Tabs**  
Review the different tabs in the **Proxy** interface to understand available options for analysis.  

<img width="567" alt="image" src="https://github.com/user-attachments/assets/7e903ee0-f4c4-48e6-a292-7d27592ee417">


---

### **7. Intercept and Forward Requests**  
Capture a request using the proxy and click **Forward** to send it to the server.  

<img width="601" alt="image" src="https://github.com/user-attachments/assets/3cd32670-390d-4223-b420-dbcd74ada564">


---

### **8. Perform Actions on the Webpage**  
Perform actions like adding an item to the wishlist or cart, and observe how Burp Suite captures the requests.  

<img width="588" alt="image" src="https://github.com/user-attachments/assets/b6ba3d14-1dc8-4b96-abcf-ef45aead8dd5">


---

### **9. Analyze Intercepted HTML Data**  
Examine the intercepted HTML request details within the Proxy tab.  

<img width="594" alt="image" src="https://github.com/user-attachments/assets/0729b848-6cdd-4550-a836-4910be4eed82">


---

### **10. Forward Requests for Additional Actions**  
Continue forwarding requests to the server as you navigate actions like proceeding to checkout.  

<img width="589" alt="image" src="https://github.com/user-attachments/assets/f3ee559f-24b0-4e6f-b910-d7b0d48d42c1">


---

### **11. Complete Checkout and Capture Requests**  
Fill out checkout details such as name and address, and capture the corresponding requests.  

<img width="597" alt="image" src="https://github.com/user-attachments/assets/82933363-2999-4878-9dcd-0abd8859a4f6">

---

### **12. Turn Off Interception**  
Disable request interception to stop capturing further actions once the necessary steps are complete.  

<img width="597" alt="image" src="https://github.com/user-attachments/assets/7e4b065b-f4d2-4dc1-921b-06dc80aabd84">


---

### **13. Use the Repeater Tool**  
Switch to the **Repeater** tab to analyze intercepted HTML requests more thoroughly.  
<img width="594" alt="image" src="https://github.com/user-attachments/assets/5bcae518-c147-4364-ba30-e94445ecd0a1">


---

### **14. Inject XML Payloads**  
Add an XML payload to include references to external entities and test for vulnerabilities.  

<img width="593" alt="image" src="https://github.com/user-attachments/assets/1b2718a8-e09c-4b0d-a435-c3617e88a702">


---

### **15. Exploit the Vulnerability**  
Replace a parameter’s value with `&payload`, send the request, and verify if the application reveals sensitive information.  

<img width="593" alt="image" src="https://github.com/user-attachments/assets/ce26c204-0bdf-4a45-ba54-6071a3d7d4ed">


---

### **16. Access User Data via XXE**  
Use crafted payloads to access user information, such as `/var/www/html/wishes/wish_21.txt`.  

<img width="599" alt="image" src="https://github.com/user-attachments/assets/48fb60d0-e82d-464d-8230-78dc283f6e30">


---

### **17. Enumerate Other User Data**  
Modify the payload (e.g., change `wish_21` to `wish_1`) to access other users’ data, including names and addresses.  

<img width="557" alt="image" src="https://github.com/user-attachments/assets/ec1b85d6-2577-42dd-9079-729baff51e59">


---

### **18. Send Requests to Intruder**  
Forward the crafted request to **Intruder** to automate attacks on multiple targets.  
<img width="594" alt="image" src="https://github.com/user-attachments/assets/fc11216b-20ed-43cb-870a-6be152f4a386">


---

### **19. Configure Intruder Payloads**  
Define the payload range (e.g., numbers 1–20) to test for vulnerabilities across multiple user accounts.  

<img width="596" alt="image" src="https://github.com/user-attachments/assets/211075b6-de2b-4a77-a8e3-6e25ed966f90">


---

### **20. Execute the Attack**  
Launch the attack from Intruder to extract data from all 20 user accounts.  

<img width="601" alt="image" src="https://github.com/user-attachments/assets/7b367683-70e1-4883-931c-68f90050e7ae">


---

## **Conclusion**  
This project demonstrates the process of identifying and exploiting XXE vulnerabilities using Burp Suite. Through systematic interception, payload crafting, and automation, sensitive user data was successfully extracted, showcasing the importance of securing XML parsers against such attacks.



