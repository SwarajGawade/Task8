# Task 8 – VPN Setup and Usage on Linux

## Objective
Understand the role of VPNs in protecting privacy and secure communication.

## Tools Used
- **VPN Client:** ProtonVPN Free Tier (CLI)
- **Operating System:** Linux (Kali in this example)
- **Browser/IP Check Tool:** [whatismyipaddress.com](https://whatismyipaddress.com)

## Steps Performed

1. **Choose VPN Provider**
   - Selected **ProtonVPN Free** plan.
   - Created a free account at: [https://protonvpn.com/free-vpn](https://protonvpn.com/free-vpn)

2. **Install ProtonVPN CLI**
   ```bash
   sudo apt update
   sudo apt install pipx
   pipx install protonvpn-cli
   ```

3. **Initialize VPN**
   ```bash
   sudo protonvpn init
   ```
   - Plan: Free
   - Protocol: UDP (faster)
   - Enter ProtonVPN username & password.

4. **Connect to VPN**
   ```bash
   sudo protonvpn c --fastest
   ```

5. **Verify IP Change**
   - Open browser and visit [whatismyipaddress.com](https://whatismyipaddress.com)
   - Confirm IP matches VPN server location.

6. **Test Encrypted Browsing**
   - Browse any website to ensure secure connection (HTTPS + VPN active).

7. **Disconnect VPN**
   ```bash
   sudo protonvpn d
   ```

8. **Compare Browsing Speed**
   - Before & after VPN connection, test at [https://www.speedtest.net](https://www.speedtest.net)

## Troubleshooting
- **HTTP Error 422** during `protonvpn init`:
  - Make sure ProtonVPN username/password are correct.
  - Ensure no special characters in password that CLI can’t parse.
  - Try logging into ProtonVPN web dashboard to confirm account works.

## VPN Benefits
- Hides real IP address.
- Encrypts internet traffic.
- Protects data on public Wi-Fi.
- Bypasses geo-restrictions.

## VPN Limitations
- May reduce browsing speed.
- Free plans have limited servers and bandwidth.
- VPN provider can still see your activity (choose trusted provider).

## Deliverables
- **Report PDF:** Task8_VPN_Report_Template.pdf  
- **Connection Status Screenshot:** Showing changed IP and VPN active.
