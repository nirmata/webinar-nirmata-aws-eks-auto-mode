# webinar-nirmata-aws-eks-auto-mode
Contains sample policies used in the Webinar on 05/28/25

## Applying Policies to EKS Auto Cluster

1. Ensure you have access to Nirmata Control Hub (NCH)
2. Navigate to the Policies section in NCH
3. Select the appropriate policy set for your EKS auto cluster
4. Apply the policies to your cluster using one of these methods:
   - Through the NCH UI: Select your cluster and apply policies
   - Using Kyverno CLI: Apply policies using `kubectl apply -f` commands
   - Using GitOps: Commit policy changes to your Git repository

## Reviewing and Fixing Policy Violations

1. Log in to Nirmata Control Hub (NCH)
2. Navigate to the Policy Reports section
3. Review the policy violations for your EKS auto cluster
4. For each violation:
   - Analyze the violation details
   - Review the suggested remediation steps
   - Apply the necessary fixes
   - Verify the remediation through NCH dashboard

## Sample Policy Structure

The repository contains the following sample policies:
- `policies/require-pod-topology-constraints.yaml`: Enforces pod topology spread constraints
- `policies/disallow-privileged-escalation.yaml`: Prevents privileged escalation in pods
- `policies/add-pdb.yaml`: Adds Pod Disruption Budgets for high availability

Additional directories:
- `resources/`: Contains resource definitions
- `rbac/`: Contains RBAC configurations

## Prerequisites

- Access to Nirmata Control Hub
- Kyverno installed in your cluster
- Appropriate RBAC permissions
- AWS EKS cluster in auto mode
