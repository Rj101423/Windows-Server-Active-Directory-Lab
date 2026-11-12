# \# Windows Server and Active Directory Home Lab

# 

# I built an isolated Windows domain in Hyper-V to practice IT support and system administration. The lab uses a Windows Server 2025 domain controller (`DC01`) and a Windows 11 Pro client (`CLIENT01`).

# 

# \## What I configured

# 

# \- Deployed Active Directory Domain Services and DNS for `ad.rjlab.test`.

# \- Joined `CLIENT01` to the domain and verified sign-in with a standard domain account.

# \- Linked a Group Policy to the `Lab Users` organizational unit. Verified that it blocked Control Panel for the domain test user while the local account retained access on the same VM.

# 

# \## Troubleshooting highlight

# 

# The client couldn’t find the domain controller because both VMs had the same static IP address. A successful ping was misleading: the client was pinging itself. I corrected the client’s address, restarted the domain controller to clear its duplicate-address status, and verified the fix with a DNS service record lookup from the client.

# 

## Documentation

- [Full project walkthrough](./Project-Documentation.txt)
- [Lab screenshots](./Screenshots/)

