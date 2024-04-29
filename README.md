### kubectl-refine

**kubectl-refine** is a handy `kubectl` plugin designed to simplify and refine YAML manifests by removing specific fields, making them cleaner and more manageable. With this plugin, you can effortlessly fetch YAML manifests from your Kubernetes cluster and refine them by eliminating unnecessary fields such as `status`, `managedFields`, `annotations`, and more.

#### Installation

1. **Download the Plugin**:
   Clone the repository or download the `kubectl-refine` script from the releases page.

2. **Make it Executable**:
   Ensure that the script is executable by running:
   ```bash
   chmod +x kubectl-refine
   ```

3. **Move to PATH**:
   Move the script to a directory in your PATH to make it accessible as a `kubectl` command:
   ```bash
   sudo mv kubectl-refine /usr/local/bin
   ```

#### Usage

```bash
kubectl refine <resource>
```

Replace `<resource>` with the Kubernetes resource type you want to retrieve (e.g., `pods`, `deployments`, etc.).

#### Example

To refine the YAML manifest for a Pod:

```bash
kubectl refine pod <pod_name>
```

This will fetch the YAML manifest for the specified Pod, remove unnecessary fields, and print the refined YAML to the standard output.

#### Dependencies

- **kubectl**: Ensure that `kubectl` is installed and configured to communicate with your Kubernetes cluster.
- **yq**: This plugin relies on `yq` for YAML processing. Make sure it's installed and available in your PATH.

#### Disclaimer

This plugin is provided as-is, without any warranties or guarantees. Use it at your own risk, and always review the modified YAML before applying it to your Kubernetes cluster.


