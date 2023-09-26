# Creating Back-End Pools 

In the context of load balancers, back-end pools play a crucial role in distributing traffic effectively. These pools contain the IP addresses of virtual Network Interface Cards (NICs) that are connected to your load balancer, and their configuration can be managed through the Azure portal.

## Things to Know about Back-End Pools

Here are some key points to understand about back-end pools:

- **SKU Determines Configuration**: The type of SKU you choose for your load balancer affects the configuration options available for your back-end pool, as well as the maximum number of pool instances allowed.

- **Pool Limits**: The Basic SKU supports up to 300 pools, while the Standard SKU allows up to 1,000 pools.

- **Configuration Options**: When configuring back-end pools, you have the flexibility to connect to various resources, including availability sets, virtual machines, or Azure Virtual Machine Scale Sets.

- **Basic SKU Configuration**: For the Basic SKU, you can select virtual machines either in a single availability set or virtual machines within an instance of Azure Virtual Machine Scale Sets.

- **Standard SKU Configuration**: With the Standard SKU, you have the option to select virtual machines or Virtual Machine Scale Sets within a single virtual network. Your configuration can include a mix of virtual machines, availability sets, and Virtual Machine Scale Sets.

These back-end pools are essential for load balancing traffic across your resources and can be tailored to your specific requirements based on the SKU type you choose.
