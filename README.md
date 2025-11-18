Task 4: Setup and Use a Firewall on Windows/Linux
Objective:
Configure and test basic firewall rules to allow or block traffic using Windows Firewall or UFW.
Tools Used:
- Windows Defender Firewall
- PowerShell
- Test-NetConnection
Windows Firewall Steps:
1. Open Windows Defender Firewall with Advanced Security.
2. Create New Inbound Rule → Port → TCP → Port 23 → Block the connection.
3. Test using: Test-NetConnection -ComputerName localhost -Port 23
4. Remove the rule after testing.
Expected Output When Blocked:
TcpTestSucceeded : False
Optional Linux UFW:
sudo ufw enable
sudo ufw deny 23/tcp
sudo ufw delete deny 23/tcp
Summary:
Blocked port 23, verified using PowerShell, restored firewall to original state.
