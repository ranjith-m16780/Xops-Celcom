⚡ XOps Microchallenge #8 – ConfigMaps vs Secrets ⚡
Hello XOps Team,
In the last challenge, you learned how to secure sensitive data using Kubernetes Secrets. Now let’s move one step further and understand how to handle application configurations that are non-sensitive – such as environment settings, feature flags, and application properties.
This challenge will help you clearly understand the difference between ConfigMaps and Secrets, and when to use each 🚀.
🎯 Objective
Show how to manage non-sensitive configs (like app.properties, feature flags, or environment variables) using Kubernetes ConfigMaps, and compare with Secrets.
🔧 Step-by-Step Challenge
1. Create a ConfigMap
Create a ConfigMap named app-config with values like:
           APP_MODE=dev
           FEATURE_X_ENABLED=true
Verify it is created successfully.
2. Inject ConfigMap as Environment Variables
Create a pod (e.g., NGINX or a simple app) that loads values from the ConfigMap as environment variables.
Use kubectl exec to confirm the values are injected.
3. Inject ConfigMap as Mounted Files (Optional)
Mount the ConfigMap into /etc/config.
Verify that the pod has files created with the config values.
4. Compare with Secrets
Create a quick Secret (e.g., fake DB credentials) and inject it the same way.
In your README.md, document:
When to use ConfigMaps vs Secrets
Best practices (e.g., never store sensitive data in ConfigMaps)
📂 Expected Repo Structure
/infra-repo
└── k8s/
    ├── configmap.yaml          # ConfigMap definition
    ├── config-env-pod.yaml     # Pod using ConfigMap as env vars
    ├── config-vol-pod.yaml     # Pod mounting ConfigMap as files (optional)
    ├── secret.yaml             # (Optional) Secret definition for comparison
    ├── secret-pod.yaml         # (Optional) Pod using secret
    └── README.md               # Steps + comparison + screenshots
✅ Submission Format
In the Teams thread, share:
✅ Link to your repo with YAML files
✅ Screenshot of pod env showing ConfigMap values
✅ Screenshot of mounted files (optional)
✅ Short note comparing ConfigMaps vs Secrets
⏳ Timeline
Start Date: 29 September 2025 (Monday)
Deadline: 06 October 2025 (Monday)
 