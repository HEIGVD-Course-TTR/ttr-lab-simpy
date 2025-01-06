Lab report: capacity planning and performance analysis with SimPy
========================================================================

> [!NOTE]
> Write your report in this document. You can write it in English or French

Result table
------------

This table documents the results of the different simulation scenarios

| Case                                                   | Required service rate| Mean service time | Response time      |
|--------------------------------------------------------|----------------------|-------------------|--------------------|
| 1a. Base scenario: $\lambda = 90/s$                    | $\mu = 100 /s$       | $1/\mu$ = 10 ms   | mean: 100 ms       |
| 1b. M/M/1 model for $\lambda = 180/s$                  | $\mu =     /s$       | $1/\mu$ =      ms | mean: 100 ms       |
| 2a. Batch arrivals with $\lambda_\text{file} = 90$/s   | $\mu =     /s$       | $1/\mu$ =      ms | mean: 100 ms       |
| 2b. Batch arrivals with $\lambda_\text{file} = 180$/s  | $\mu =     /s$       | $1/\mu$ =      ms | mean: 100 ms       |
| 3a. Batch arrivals with $\lambda_\text{file} = 90$/s   | $\mu =     /s$       | $1/\mu$ =      ms | 99th perc.: 300 ms |
| 3b. Batch arrivals with $\lambda_\text{file} = 180$/s  | $\mu =     /s$       | $1/\mu$ =      ms | 99th perc.: 300 ms |



Case 1a: Base scenario
----------------------

Scenario

- M/M/1 model
- $\lambda = 90$ requests per second
- Target response time $E[t] = 100$ ms

Use the analytical model to compute required service rate $\mu$. Report the value in the table on top.



Case 1b: Doubling the arrival rate
----------------------------------

Use the same scenario as in Case 1a, but double the arrival rate $\lambda$.

Use the analytical model to compute the required service rate $\mu$. Report it in the table on top.

**Questions**: 

- Does the service rate need to double, too?
- What happens if you double the service rate?
- Interpret the result.



Case 2a: Batch arrivals
-----------------------

Simulate the model with batch arrivals and an arrival rate of Web pages $\lambda_\text{web}$ chosen such that the arrival rate of file downloads is $\lambda_\text{file} = 90$ file requests per second.

**Questions**:

- Which service rate is required to achieve a mean response time of $E[t] = 100$ ms. Report this result in the table on top.
- Interpret this result!



Case 2b: Batch arrivals and double arrival rate
-----------------------------------------------

Determine the service rate \$mu$ that is required if the arrival rate of Web pages doubles and we want to achieve a response time of 100 ms.

**Questions**:

- Report required service rate in the table on top.
- Interpret the result.



Case 3a: Batch arrivals and 99th percentile
-------------------------------------------

Determine the service rate $\mu$ that is required such that the 99th percentile of the response time is around 300 ms.


**Questions**:

- Report this result in the table on top.
- Interpret the result.



Case 3b: Batch arrivals, double arrival rate and 99th percentile
----------------------------------------------------------------

Determine the service rate \$mu$ that is required if the arrival rate of Web pages doubles such that the 99th percentile of the response time is again around 300 ms.

**Questions**:

- Report this result in the table on top.



Visualization
-------------

Use the plot functions defined in the file `visualization/plots.py` to visualize the response time distribution for the case 3b (Batch arrivals, double arrival rate and 99th percentile).

**Questions**:

- Include each plot in this report. 
- Explain how each plot can be used and its limitations.


Conclusion
----------

Document your conclusions here. What did you learn from the simulation results?
