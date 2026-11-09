# Group Policy Configuration

## 1. Overview
Group Policy was used to apply security and administrative settings to users in the **lab.local** Active Directory domain.

The lab uses Windows Server 2022 as the domain controller and Windows 11 Pro as the client workstation.

## 2. Control Panel Restriction
A Group Policy Object (GPO) named **IT - Block Control Panel** was created and linked to the IT-Department OU.

### Configuration path:
User Configuration → Policies → Administrative Templates → Control Panel

* **Policy:** Prohibit access to Control Panel and PC settings
* **Setting:** Enabled

### Verification
On the Windows 11 client (CLIENT01):
1. Ran `gpupdate /force`.
2. Signed out and signed back in.
3. Tested access to Control Panel.

**Result:** Access to Control Panel and PC settings was successfully blocked for the affected user.

## 3. Domain Password Policy
The Default Domain Policy was configured with the following password settings:

| Policy | Configured Value |
| :--- | :--- |
| Enforce password history | 5 passwords |
| Maximum password age | 90 days |
| Minimum password age | 1 day |
| Minimum password length | 12 characters |
| Password must meet complexity requirements | Enabled |
| Store passwords using reversible encryption | Disabled |

These are the settings used in this learning lab.

## 4. Account Lockout Policy
The Default Domain Policy was configured with the following values:

| Policy | Configured Value |
| :--- | :--- |
| Account lockout threshold | 5 invalid attempts |
| Account lockout duration | 5 minutes |
| Reset account lockout counter after | 5 minutes |

The configuration was checked using PowerShell and the `net accounts /domain` command.

Further account lockout testing and troubleshooting remain to be completed.

## 5. Verification Commands
The following commands were used during policy verification:

Force Group Policy update:
```bash
gpupdate /force
```

View applied Group Policy settings:
```bash
gpresult /r
```

Check domain account policies:
```bash
net accounts /domain
```

Check Active Directory password and lockout policy:
```powershell
Get-ADDefaultDomainPasswordPolicy
```

## 6. Skills Practised
* Creating and linking Group Policy Objects.
* Configuring user restrictions.
* Managing domain password requirements.
* Configuring account lockout settings.
* Updating and verifying Group Policy.
* Using PowerShell for policy verification.

## 7. Next Steps
* Complete account lockout testing.
* Practise additional GPO security settings.
* Document further Windows Server administration exercises.
