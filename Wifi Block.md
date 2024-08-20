# **WiFi Configuration 📡**

To set up and block specific websites on your WiFi router (**Model: TL-WR841N / TL-WR841ND**), follow these step-by-step instructions:

**Model No: TL-WR841N / TL-WR841ND**
   <!-- 
   - **Username:** Manojmishra
   - **Password:** india 

   - in **Advanced**
   - Service Name : HATHWAY    -->


## **WiFi Block Tutorial 🚧**

For a detailed tutorial on blocking WiFi access to specific websites, you can watch the following video:

- [WiFi Block Tutorial](https://www.youtube.com/watch?v=pAqUrzYCzh0&ab_channel=tutorialplus) 🔗

### **Router Configuration Steps:**

1. Open your web browser and go to `http://192.168.0.1/`. 🌐
2. Enter your router's username and password on the login page. 🔐

### **Access Control Setup:**

3. Navigate to the `Access Control` section and click on `Setup wizard`.
   - Set the following details:
     - **Mode:** `IP Address`
     - **Host Description:** `Some Description`
     - **LAN IP Address Range:** `192.168.0.2` to `192.168.0.254`

4. Click "Next" to proceed. ➡️

### **Domain Name Configuration:**

5. On the next page, fill in the following details:
   - **Mode:** `Domain Name`
   - **Target Description:** `Some Description`
   - **Domain Name:** Add the websites you want to block (e.g., `mangakakalot.com`, `mangahub.io`).

6. Click "Next" to proceed. ➡️

### **Access Schedule Setup:**

7. Fill in the following details:
   - **Schedule Description:** `Some Description`
   - **Day:** Select `Everyday`
   - **Time:** Select `All day - 24 hours`

8. Click "Next" to proceed. ➡️

### **Access Control Configuration:**

9. Back in the `Access Control` page, enable "Internet Access Control."
   - Set the `Default Filter Policy` to "Deny the packets specified by any enabled access control policy to pass through the Router."

10. Save the configuration. 💾

Now, the websites specified in the `Domain Name` section will be blocked according to the schedule you've set. The internet access control policy will restrict access during the specified times. 🚫
