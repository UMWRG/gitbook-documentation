# Allocation Penalties

Allocation penalties are node attributes that allow Pywr to simulate water allocation. They can also be called 'allocation priorities' or 'costs'.

A low penalty will have the highest allocation priority, a high number has the lowest.&#x20;

So for example if three nodes have priorities 100, 3, and -2, then the node with -2 gets its water first, then 3, then 100.

Here are some questions about water allocation penalties you may have, and some short answers:

1. Why and how does Pywr allocate water like this? At each time step Pywr's allocation algorithm (a linear program), minimizes the allocation penalty of the entire system. Flow through nodes is multiplied by their respective allocation penalties. This technique has been in use since the 1950s by energy, transport and water planners and by logistics companies. They all want systems that operate cheaply, so they typically used financial operating costs as the penalty term. This makes sense, it allows using the model to balance a supply-demand network at the lowest cost.&#x20;
2. Do you find the idea of a negative penalty confusing? If so, think of a negative penalty as a negative cost, what's that? a benefit!  So if you'd like to allocate water to where it generates the most benefits in your Pywr model, you'll be using negative penalties.  In this case, rather than calling these node attributes allocation penalties or costs, you could refer to them as allocation priorities. In this case a node with an allocation priority of -99 will get water long before -10. As shown in the example in the third sentence above, both negative and positive allocation penalties can be used in the same model.
3. Do allocation penalties have some special meaning? No, they don't. They are just there to help your model allocate water in a way that make sense to you, the water manager and planner. &#x20;
4. How do I know if i've set water allocation penalties correctly? If your model is allocating water appropriately under normal conditions, but also during floods and droughts, then you have set appropriate penalities. Congratulations! your model is on its way to becoming 'well-calibrated'.
5. If I make a big change to my model, like add a large new infrastructure, or add a new water user-type, do i need to change the penalties in my model? Yes, some penalties in your model might need some refinement, depending on how significant the change is. Try and see.
6. Can i use any numbers for penalties? like, if my model has 2 nodes, can i use negative and positive one million as my penalties? Yes, but it's a bad idea. Use numbers that are as close together as you can. If not, as your model grows, you could run out of available penalties and your model will begin to make round-off errors. However, if you use penalities that are too similar, your model might be insensitive to them (i.e., not consider them adequately when simulating allocations). With a bit of experience you'll learn to set penalities that work well. To gain that experience, try changing penalties and see how it affects your model's outputs.

Finally, we provide a few more technical details about penalities:&#x20;

* Reservoir and storage nodes have allocation penalties assigned to them. A negative penalty means the reservoir will tend to accumulate water, unless a lower penalty on another node results in the reservoir storage having lower priority. &#x20;
* Allocation penalties can be constants (constant parameters) or profiles (monthly, daily, weekly) that change over time. Also, allocation penalties can have different levels defined by different control curves based on the reservoir volume. Despite the reservoir and storage allocation penalties influencing water storage, releases from those nodes will result from a penalty balance in the system considering allocation penalties downstream as the algorithm attempts to minimse the overall system penalty at each time step.

{% embed url="https://youtu.be/bJ6FlQ103BU" %}
