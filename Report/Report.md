# Setup and Use a Firewall on Linux (UFW)

## Objective

Configure and test basic firewall rules to allow or block traffic.

## Tools Used

* **Linux:** UFW (Uncomplicated Firewall)

## Steps Performed

### On Linux (UFW)

1. **Install UFW**

   ```bash
   sudo apt install ufw
   ```

2. **Set Default Policies**

   * Deny all incoming traffic:

     ```bash
     sudo ufw default deny incoming
     ```
   * Allow all outgoing traffic:

     ```bash
     sudo ufw default allow outgoing
     ```

3. **Allow SSH (Port 22)**

   ```bash
   sudo ufw allow 22/tcp
   ```

4. **Enable UFW**

   ```bash
   sudo ufw --force enable
   ```

5. **Check Firewall Status (Verbose)**

   ```bash
   sudo ufw status verbose
   ```

6. **Verify Open Ports with ss**

   ```bash
   sudo ss -tuln
   ```

<img width="719" height="372" alt="Image" src="https://github.com/Gautam-CyberSec/Setup-and-Use-a-Firewall-on-Windows-Linux/blob/main/Screenshots/Screenshot%202025-09-16%20155803.png" />

## Conclusion

The firewall was successfully configured using UFW on Linux. By applying a default deny-all policy for incoming traffic and allowing outgoing connections, the system is secured against unauthorized access. Specific rules, such as permitting SSH on port 22, ensure required services remain accessible. Verification with ufw status verbose and ss -tuln confirmed that the firewall rules were applied correctly and the system is functioning as intended
