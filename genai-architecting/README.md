# Functional Requirements
The company wants to avoid vendor lockin. This applies to the model being used, and the infrastructure. 

They would like to use their current Kubernetes cluster if that is a viable option with the addition of nodes with GPUs. 
If running locally on their Kubernetes cluster is not viable, they would like to be able to be able to run this in the cloud, without being tied to a specific cloud platform.

# Considerations
We will be using LLama 3.1 8b as the baseline since this is the model we have the most experience with, and will be guaging its performance in comparison to DeepSeek R1 7b.
