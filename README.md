# ACTIVE-DIRECTORY--GPO-LAB
Windows server active-directory- lab demonstrating secure and practical Group Policy management.This project demonstrates how GPOs can be used to improve endpoint security, standardize workstation configurations, and streamline administrative tasks in an enterprise setting .

LAB ENVIRONMENT
Domain name: stanbic.com
Domain controller: Windows server 2016
Clients machine: windows 10 pro
Virtualization platform: VMware workstation
Network Layout; one domain controller, multiple client machines


OBJECTIVES
Create an organized Active Directory OU structure
configure password and account lockout policies
restrict access to control panel 
configure windows defender and firewall
deploy mapped network drives 
configure windows updates policies 
apply security baseline to workstations
test policy inheritance and enforcement

OU STRUCTURE
Stanbic.com
  users
    finance
    HR
    IT
  Computers
    workstations
    laptops
    servers


  EXAMPLE GPO Documentation
  Workstation security baseline
   Purpose: Apply basic security settings to all domain workstations 
   Linked OU; OU=Workstations,DC=stanbic DC=.com
    settings;
    require complex passwords
    enable windows firewall
    configure automatic screen lock
    enable Microsoft defender
    prevent users from disabling security settings

    testing;
    ran "gpupdate /force"
    verified with "gpresult /r"
    confirmed results using resultant set of policy (RSoP)

    Result
    policy successfully applied to test workstations
    
    
