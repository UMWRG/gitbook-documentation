# Allocation Penalties

Allocation penalties are node attributes that allow Pywr to simulate water allocation. They can also be called 'allocation priorities' or 'costs'.

A low penalty will have the highest allocation priority, a high number has the lowest.&#x20;

So for example if three nodes have priorities 100, 3, and -2, then the node with -2 gets its water first, then 3, then 100.

Why does it work like this? At each time step the allocation algorithm (a linear program), minimizes the allocation penalty of the entire system. Flow through nodes is multiplied by their respective allocation penalties. This technique was used since the 1950s by enery, transport and water planners. They all want systems that operate cheaply, so they typically used financial operating costs as the penalty term. This makes sense, it allows using the model to balance a supply-demand network at the lowest cost.&#x20;

Do you find the idea of a negative penalty confusing? Think of a negative penalty as a negative cost, what's that? a benefit!  So if you'd like to allocate water where it generates the most benefits in your Pywr model, you'll be using all negative numbers.  In this case, rather than calling these node attributes allocation penalties or costs, you can refer to them as allocation priorities. In this case a node with an allocation priority of -99 will get water long before -10.

Reservoir and storage nodes have allocation penalties assigned to them. A negative penalty means the reservoir will tend to accumulate water, unless a lower penalty on another node results in the reservoir storage having lower priority. &#x20;

Allocation penalties can be constants (constant parameters) or profiles (monthly, daily, weekly) that change over time. Also, allocation penalties can have different levels defined by different control curves based on the reservoir volume. Despite the reservoir and storage allocation penalties influencing water storage, releases from those nodes will result from a penalty balance in the system considering allocation penalties downstream as the algorithm attempts to minimse the overall system penalty at each time step.

{% embed url="https://youtu.be/bJ6FlQ103BU" %}
