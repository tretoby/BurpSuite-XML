# **Burp Suite Project: Identifying and Exploiting XXE Vulnerabilities**

## **Task**  
Leverage **Burp Suite** to intercept and analyze web page requests, identify potential XML External Entity (XXE) vulnerabilities, and execute a targeted attack to extract sensitive information from 20 user accounts.

---

## **Steps**

### **1. Launch Burp Suite**  
Begin by starting Burp Suite to initialize the testing environment.  
![image](https://github.com/user-attachments/assets/3bcc2a4f-59de-4fc2-b707-3c1dfb38196e)

---

### **2. Access the Proxy Tab**  
Navigate to the **Proxy** tab to enable interception of requests between the browser and the server.  
![image](https://github.com/user-attachments/assets/dc0793a1-42c7-46c8-94eb-1cfad961b81a)

---

### **3. Open the Burp Suite Browser**  
Use the Burp Suite browser to interact with the target web application for testing.  
![image](https://github.com/user-attachments/assets/dcbbe82c-e725-4233-87ae-cc2630fe9bc3)

---

### **4. Navigate to the Target Webpage**  
Access the webpage through the **Burp Browser**, preparing for analysis and testing.  
![image](https://github.com/user-attachments/assets/41e74e0f-f034-4409-ad00-7c538a22b5eb)

---

### **5. Enable Request Interception**  
Return to the **Proxy** tab and enable **Intercept** to capture HTTP requests.  
![image](https://github.com/user-attachments/assets/955976bf-351d-4541-8784-8fdb42ccfc4f)

---

### **6. Familiarize Yourself with the Proxy Tabs**  
Review the different tabs in the **Proxy** interface to understand available options for analysis.  
![image](https://github.com/user-attachments/assets/c5f51cba-b01d-4eed-b672-2f7dde9fc149)

---

### **7. Intercept and Forward Requests**  
Capture a request using the proxy and click **Forward** to send it to the server.  
![image](https://github.com/user-attachments/assets/9afb8580-a136-4d8f-a102-4e130830ac22)

---

### **8. Perform Actions on the Webpage**  
Perform actions like adding an item to the wishlist or cart, and observe how Burp Suite captures the requests.  
![image](https://github.com/user-attachments/assets/68f76a9f-3f44-4e7b-8afa-bf4c110ffc7f)

---

### **9. Analyze Intercepted HTML Data**  
Examine the intercepted HTML request details within the Proxy tab.  
![image](https://github.com/user-attachments/assets/31a1b325-5435-4773-960b-bdcc5775dbb4)

---

### **10. Forward Requests for Additional Actions**  
Continue forwarding requests to the server as you navigate actions like proceeding to checkout.  
![image](https://github.com/user-attachments/assets/a480e49f-8dab-4017-9019-47b27e85daab)

---

### **11. Complete Checkout and Capture Requests**  
Fill out checkout details such as name and address, and capture the corresponding requests.  
![image](https://github.com/user-attachments/assets/39f8e840-01b4-442e-9e76-53fa6ae08525)

---

### **12. Turn Off Interception**  
Disable request interception to stop capturing further actions once the necessary steps are complete.  
![image](https://github.com/user-attachments/assets/3bb1b1f5-6154-42a6-ba3b-c46bd0b7bfeb)

---

### **13. Use the Repeater Tool**  
Switch to the **Repeater** tab to analyze intercepted HTML requests more thoroughly.  
![image](https://github.com/user-attachments/assets/9271221f-09af-4671-a1be-ef858bd4723a)

---

### **14. Inject XML Payloads**  
Add an XML payload to include references to external entities and test for vulnerabilities.  
![image](https://github.com/user-attachments/assets/0b15ff1e-b467-4749-8860-341b061c2772)

---

### **15. Exploit the Vulnerability**  
Replace a parameter’s value with `&payload`, send the request, and verify if the application reveals sensitive information.  
![image](https://github.com/user-attachments/assets/50942556-9405-4a7e-baaa-25d78ae2be6d)

---

### **16. Access User Data via XXE**  
Use crafted payloads to access user information, such as `/var/www/html/wishes/wish_21.txt`.  
![image](https://github.com/user-attachments/assets/9eef8b84-37cb-4440-845b-d3832eb4e6dc)

---

### **17. Enumerate Other User Data**  
Modify the payload (e.g., change `wish_21` to `wish_1`) to access other users’ data, including names and addresses.  
![image](https://github.com/user-attachments/assets/d429054f-041a-483d-ae57-531d3dd8d468)

---

### **18. Send Requests to Intruder**  
Forward the crafted request to **Intruder** to automate attacks on multiple targets.  
![image](https://github.com/user-attachments/assets/40e6848e-fe59-441e-ad03-bf5876ee4f4f)

---

### **19. Configure Intruder Payloads**  
Define the payload range (e.g., numbers 1–20) to test for vulnerabilities across multiple user accounts.  
![image](https://github.com/user-attachments/assets/f55d011a-5654-4552-99e9-74566858d3df)

---

### **20. Execute the Attack**  
Launch the attack from Intruder to extract data from all 20 user accounts.  
![image](https://github.com/user-attachments/assets/96774249-9ab0-492c-9b63-281c7e9b7284)

---

## **Conclusion**  
This project demonstrates the process of identifying and exploiting XXE vulnerabilities using Burp Suite. Through systematic interception, payload crafting, and automation, sensitive user data was successfully extracted, showcasing the importance of securing XML parsers against such attacks.



