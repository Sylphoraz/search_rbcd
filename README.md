# Foreword

The primary method for executing RBCD attacks currently involves searching for `mS-DS-CreatorSID`. If the machine creator is under our control, we can modify the corresponding machine's `msDS-AllowedToActOnBehalfOfOtherIdentity` setting using the tool [SharpAllowedToAct-Modify].



Then let's go ahead and try searching all computers to check their `msDS-AllowedToActOnBehalfOfOtherIdentity` attribute. If any values point to machines or accounts we control, we can simply use RBCD to take them over.

# Usage

`python3 search_rbcd.py  -u ldapusername -p 'ldappassword' -d domain.com -l ldapserver.domain`



<img width="1182" height="177" alt="image-20220115233019823" src="https://github.com/user-attachments/assets/a3acea79-e36c-4f7d-a734-558f065decb9" />