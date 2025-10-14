
# 🛡️ Suricata Detection: External IP Lookup

## 🧠 Overview
This project demonstrates live packet inspection using Suricata in Docker, rule injection, and alert validation. It includes a custom rule for `testmyids.com` and confirms detection via `fast.log`.

## 📸 Suricata Detection Pipeline Artifacts

Below are key screenshots captured during the Suricata lab deployment and validation process:

### 🧱 Suricata Container Launch
![Suricata Container Launch](screenshots/suricata_container_launch.png)

### 🔄 Rule Update Confirmation
![Rule Update Confirmation](screenshots/rule_update_confirmation.png)
![Rule Update Confirmation](screenshots/rule_update_confirmation(2).png)

### 🧩 Merge Custom Rule into Active Ruleset
![Merge Custom Rule](screenshots/merge_custom_rule.png)

### 🚨 Alert in fast.log
![Alert in fast.log](screenshots/alert_fastlog.png)


### 🕵️ Caldera Timeline
![Caldera Timeline](screenshots/caldera_timeline.png)


## 🔗 GitHub Repository
➡️ [View on GitHub](https://github.com/DevinClements/suricata-detection)

## 🛠️ Environment
- **Interface**: `ens160`
- **Container**: `jasonish/suricata:latest`
- **Rule Source**: `suricata-update` (ET + GPL)
- **Custom Rule**: `testmyids.com` (SID: 9999999)

## 🚀 Setup Commands

### Update Rules
```bash
docker run --rm -it \
  -v /var/lib/suricata:/var/lib/suricata \
  jasonish/suricata:latest suricata-update



