# 3-stage-pipeline-processor
1. Introduction:
The introduction introduces the significance of pipelining in CPU architecture and emphasizes the importance of managing control hazards in such systems. It highlights the role of CSR and outlines the project's objectives and scope.

2. Literature Review:
This section thoroughly reviews and synthesizes existing literature on pipelining architectures, control hazard mitigation strategies, and the integration of CSR. It critically analyzes previous methodologies, highlighting their strengths and limitations.

3. Architecture Design:
An intricate exploration of the design principles behind a three-stage pipelining system is presented. A detailed breakdown of the instruction fetch, decode, and execute stages is provided, elucidating how CSR is seamlessly integrated into this architecture.

4. Implementation:
The implementation phase is described, encompassing the tools, programming languages, and platforms utilized. Challenges faced during implementation are outlined alongside the strategies employed to overcome them.

5. Control Hazard Mitigation Techniques:
Various sophisticated techniques deployed to counter control hazards within the three-stage pipeline are thoroughly explained. This section includes a comparative analysis of stall mechanisms, branch prediction strategies, and other innovative solutions.

6. CSR Integration:
Detailed insights into the incorporation of Control and Status Register within the pipelined architecture are provided. This includes an exploration of CSR's functionalities, its interaction with pipeline stages, and the advantages gained from its integration.

7. Challenges and Optimizations:
Challenges Faced:
Control Hazard Handling: Managing control hazards within a three-stage pipelining system posed a significant challenge. Resolving branches at the decode stage and ensuring seamless instruction flow without stalls was complex.

Pipeline Stall Minimization: Overcoming stalls in the pipeline caused by dependencies or hazards demanded intricate solutions to maintain pipeline efficiency without sacrificing performance.

CSR Integration Complexity: Integrating the Control and Status Register (CSR) without disrupting the existing pipeline flow and ensuring its functionalities added complexity to the design and implementation process.

Instruction Scheduling: Optimizing instruction scheduling to avoid hazards and ensure maximum pipeline utilization while balancing the complexity of scheduling algorithms was challenging.

Optimization Strategies:
Forwarding Mechanisms: Implementing efficient forwarding logic to transmit necessary data between pipeline stages reduced stalls caused by data hazards, enhancing overall throughput.

Branch Prediction Algorithms: Employing advanced branch prediction techniques, such as dynamic predictors or pattern-based predictors, to mitigate control hazards and reduce pipeline stalls caused by mispredicted branches.

Pipeline Interlocking: Introducing interlocking mechanisms to prevent hazards, enabling simultaneous instruction execution when dependencies arise, thereby minimizing stalls without compromising correctness.

Instruction Reordering: Implementing intelligent instruction reordering techniques to optimize instruction sequences, reducing dependencies and hazards, and thereby minimizing stalls in the pipeline.

Hardware-Level Optimization: Leveraging hardware-level optimizations, such as parallel execution units or enhanced instruction fetching mechanisms, to exploit instruction-level parallelism and enhance overall system performance.

Dynamic Instruction Scheduling: Implementing dynamic scheduling algorithms to dynamically reorder instructions based on run-time conditions, mitigating hazards and improving pipeline efficiency.

CSR Streamlining: Streamlining the Control and Status Register's functionalities to minimize its impact on pipeline stages and reduce potential delays caused by CSR operations.

Performance Profiling and Analysis: Conducting extensive performance profiling and analysis to identify bottlenecks and fine-tune the pipeline design and optimization strategies accordingly.

8. Performance Evaluation:
Performance evaluation metrics, such as throughput, latency, and cycles per instruction (CPI), are defined and applied to assess the system's efficiency.
 Performance Metrics:
Throughput: Measure the rate at which instructions are completed per unit of time to assess the system's overall processing capability.

Latency: Evaluate the time taken for a single instruction to complete its execution cycle through the pipeline, providing insights into system responsiveness.

CPI (Cycles Per Instruction): Calculate the average number of clock cycles required to execute an instruction, a crucial metric in assessing system efficiency.

Experimental Setup:
Simulations: Conduct simulations using appropriate tools (e.g., Verilog, SystemVerilog) to model and simulate the pipelined architecture under various workloads and scenarios.

Test Cases: Develop a comprehensive set of test cases covering diverse instruction types, data dependencies, and branching scenarios to evaluate the system's performance comprehensively.

Workload Variation: Utilize different workloads, ranging from simple to complex instruction mixes, to assess the system's performance under varying computational demands.

Performance Evaluation Strategies:
Baseline Measurements: Establish baseline performance metrics for the three-stage pipelined architecture without optimizations or hazard mitigation techniques to quantify improvements achieved.

Impact of Hazard Mitigation: Evaluate the impact of control hazard mitigation strategies on pipeline efficiency and performance metrics, comparing scenarios with and without hazard handling mechanisms.

Optimization Analysis: Measure the effects of optimization strategies (e.g., forwarding, branch prediction) on pipeline stalls, throughput, and CPI to quantify their contributions to performance enhancement.

CSR Overhead Analysis: Assess the impact of CSR integration on performance metrics, examining any latency or throughput variations resulting from CSR operations.

Result Analysis:
Data Interpretation: Analyze collected performance data, graphs, and metrics to draw correlations between different strategies, optimizations, and their effects on system performance.

Comparison and Validation: Compare the obtained results against theoretical expectations and prior simulations, validating the effectiveness of implemented strategies.

Identifying Bottlenecks: Identify any performance bottlenecks or limitations within the system, pinpointing areas that may require further optimization or improvement.

Conclusion from Performance Evaluation:
Performance Impact Summary: Summarize the impact of control hazard mitigation techniques, CSR integration, and optimization strategies on system performance.

Achievement Assessment: Evaluate the extent to which the objectives set out in the introduction were accomplished based on the performance evaluation results.

Future Considerations: Discuss potential further optimizations or enhancements based on identified bottlenecks or areas with room for improvement highlighted during the evaluation


LINK FOR DIAGRAM: 
https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&edit=_blank&layers=1&nav=1&title=riscv_single%20cycle.drawio#R7V1tc6y2kv41rv1kCgkhwcdjO05Sm1SdJHfv7v3kwh5sz57xMJfBx3Z%2B%2FYUZhKERIEASzBmcSuIBxGD6Rd2tpx9dONcv7z%2FHwe7592gVbi6wvXq%2FcG4uMMaIeun%2FsiMfxyOui44HnuL16niodOCv9d9hftDOj76uV%2BG%2BcmESRZtkvasefIi22%2FAhqRwL4jh6q172GG2q37oLnsLagb8egk396P%2BuV8nz8ajn2p%2FHfwnXT8%2F8m5Gdn3kJ%2BMX5gf1zsIreSoecny6c6ziKkuNvL%2B%2FX4SZ7efy9HMfdNpwtHiwOt4nMgJ9ef7W3653H3r69%2FvObS71frr9e5nf5Hmxe8z84f9jkg7%2BBcJW%2BkPxjFCfP0VO0DTY%2FfR69Sv%2ByXXY2l0EUp8fi6HW7CrOvttNPn%2BN%2Bi6JdehClB%2F8%2FTJKPXOLBaxKlh56Tl01%2BNnxfJ%2F%2BXDbfc%2FNO%2FSmdu3vM7Hz58lD58DeP1S5iEcX5sE9yHm6vg4dvT4ZGuo032fDer8DF43STZ0ydx9C3kxy%2Bw8%2Fhopz%2FpmWCzftpmf1f6hrP7XX0P42Sd6saX%2FMTLerU6vIHHaJvcBi%2FrTfYkv4Sb72F2XX4i%2FxMRyj%2FXHyHcrr5kupq94V24PRxJ4o%2FSn599LP7%2B7MPnCzh8%2Bih%2Fgq8gvf3terPJP9X1httVED%2BFSYuyOMfrMoUoDcy17ecwSr8z%2FkgviMNNkKy%2FVy0oyA3xqbiuGPo1WqePgu3caRCXpH%2F0YVDuNAi3IX6TffQaP4T5uE%2BdT38pPcjnoYMl9LAKLLAKepBUJr%2BDt%2BHaQv%2F9mhnw1afelA7Rp%2Bz%2F8eNdKtP8BunzHO9xPCe0tt8yla1ag7wqxuF%2B%2FXdwf7hfJu5d9pIOr829unBvGnSyUXnrylrXnzbPkvuE%2FIE%2BvWH2%2FOF7qxrlZy9tizl%2BrhBDVStXJFodED0%2B7kMtGuQ0atB9Rd5cV7JXfbk%2FCOVLeoG3ez8qEFClP8On9T5TgOw15veL%2BcnUxsOSmt036ljVN789r5Pwr13wkJ19S2fxquZV9ecq%2Fd7r6r%2BpTuFrfsbCbsvJtnOs%2BSQSn4HfJTjZNLJtYNs41jaQNY9EjcNQ21tDLW%2FteI46LScbXikSPebBMzRODfLWSuyq6y4M%2Fu0zeipipOdy5MTsZmuumGdfWyR6bPHXbRo5vD4k62grNMffw5coe3rVBqlASFRCRkgkIz5QuYzcrhl3sJhKshbIDQrtJnxIU5hYLDW5Gdy0MLEDpOkIpIlF0iS6LI4OSCKUJQz8939VkoeGhKEIs8tBdinmbgyz6wG7VIx9DFzbwiZPMhhHTHU0PkrkTJsBx3ska3qpxSRVpagmd9toe8jWUkGBQ%2FLxtcigq7qrYxYldZsWmrQui%2FY0ihcv4uXzqkC8ykXp6xPlapGkN7Gh8htrEO%2FbKkiCs5ewQ5CFajJ2jMpYpmpbi1BKoqi%2BpMFB0KCAS1GYRCTDJNkoqSRLVyBLfmxkadNxgbtwgY40FDbrNVLod2xwo%2BOL0VYhRaISqQIVvLQt2yYVPewMxUUV7ylVk0qqpjdv1YS5vrRqIhi7ghvpVk1R7XWEappNK9WooCupgv68VJABzWFDVRDDApdhFWwuOS7ZcP8QzIEVrqmzYaSvXHmGOVRNvJPnUFSj%2BZ5ftaMmXzq1fPUVK9fbfXJ2Aq6tQPhTC1hfufIsBYxgbjC5gP3ayzaxwtQAyupOUXWtFvGX3hnoY9lkU3EIT23b8pHvEjtVGs%2BTC8PTlxV8lC7LISiNX1pMKBxjygASst%2F16S%2FHJ1CLKdNXmI122aL12XmlorDAK7Nu3SuJ6rLaVlYKs51k3bsXUHZ%2BngzLejLZmoWZdW%2F%2B3BrM%2BvF1%2B5A452fWXtU7T2%2FWzmLWg81adp2GS3QuZq2vgncwa3Z2Zu2guc3W7tQ5BKvYqOU5nWYqWOpqbl8ZbNXdxorNZBPUq%2BoMkVzlrN2IYTCnQLCx7oaSzopir46S9C53qb6dW0sJt1glPSVekY2OVFIwQF9PCdZXtqyBpK%2FTcXG02RiEQi%2BNJqoaTawMndF40mkb2dpr4rec9DxdHSWwusyrNZ349homRl3ooK%2B%2BvNRyGoVsNjrUB5Nd8vp5iJh%2F2ZLjHUT8HMXrv9PHDBT2JsGkb3qZT1ailWcsaEKPYW1dSd0Jn%2FJmo0ELPZ5LLYL94serKBfOm8SbksCO0dQF2lVaBKrfyyEST2IqveT5eBvkkXuGQyb4NdqvDw2Qzs19lCTRi8B1JBEI0DnNx8v7U8b1Yt0H%2B%2FWDtYs2H0%2FZna6y366jKF7BIB7En7WQE3Qtg5C8Gr3TcuQNxh%2BvIEXwmT3QZr3laWtBwHLg9tjvjnQxj%2Bv3zLSF6YeFG%2BLz44OK4%2BFDYecQErf1ZtcCbVXhMoUgSgFYjnmHZ4ReF2lbr3cmK6F3FspZT34VXZVy7jK6OxrQLHyxSyCqy2n2n8ocHZlKj4ZDwFOXpYDAp1XrypHhBXZCtHJDVgsj0zO2ndeGh%2BspDwW6G5R50VN3lRjZlFm2SxomY8dxrHRCtvkPuL8iDIrv0eq32hVzED203zZAk%2F0MWfPQQu91brRcs47D69qMUUt4S2CcoDu8Vbt6sno5Rz4uR%2BXiicsVcSQfF28jNEDIZXDx5KbUJy3HBySni%2Fq5ZDzWmiJjxon5SsmEL6jfINjXqi6T8OYyg4kBOkUgKIwK%2B896RcQ2i1mvWpBi3QUpcTCrpskRyzbaGuKt9EDXoUuQlQafDiM2dogDmxllsQvI9l3LsxvDWxtbxP8860tNzX3D2%2FQhEPza9qdGAGTdewAh7ShuCDXve71DPAMBt2gZ6YQy2O4ySL4SUbXqUpxM0py94jWo0%2BgZBMXw4f7BFEgpNU3LL%2F2w6pwpWQoeW2FWlMYygLjqqql3XK%2FHqHhFczLkXkWjtVR0GtX%2BdMou7fOSIn1FNkD2cdBH82wKB%2FhdA0ChBgwYt1AEISqaM2kyZPlTT%2FQ8kCJjWAT9%2BDh1BF2ZHT8zh0rqYDHK2qfkoRPkHz%2Bjf%2F7xJfnjnpL%2F3r8H7PnLv79cSnsUpCeA7j83gQCRkY65CQBO0Omu8BIZUhuTc2A%2Fq9W3bObKajFRrcPjOKn19ZfUylFf4%2BgpDl7qFanrVB2S0yI7voTxputafm4b5QVuQU3KdyzuyNSLU0QIA15VEq%2BD7VMjGKtCQJUEOTrj0leEvruE6Tj20%2BCtlLY0M5AaAWaR5hp%2FSSmvxLoKHeFms97tJV50DQSi4EX7btvSCXLq71kEgHO0vWc27bxh4elyp87JhMhWFOeSZGGGLFpKslj1%2FsqSLFJ1Hry835wzgQGcyU1vWUCEyp9I1wfWzUaormyjLQ%2BYdGvuJez3zOu%2FvQthFN4HTOKaufzIxFQzcwm0kXQrNzHkGz1ELZ4XccdEbSnl6A08FnxVhw%2FsHqLHC7rTFkfRXPRVOjF051HdAIuHnOBZr65IEInz6t9b8HH4E7IS27cweXi%2B%2BMQecuXaR5vs%2B66OSepNBnw8jAnjn76HR9RLvdPz5kLY2gJxM4ekqIyjKUWFx4peKU682m%2BD3T%2Bi4ytWlnxCYmMfC%2BAQRrMmd5oIZwDyoZwBzARxzcuD3dE%2BUV486nARqoMYV1Q%2BPMXs%2BpKBMoaAidBoPu1Og0gfjkPVNd3Kti%2Bon27Hya%2BZyrkwAQf%2F14pI2cY8OjlV2BlkXhFw9lKjdjbNnnKzI9RyZdsv1Gdh4%2BTXjL89ZzvznTbAraBb2qzR6eO5CFar%2BLT64xVIG%2B676jOLl5em2kvKnba81bNcMAXZGTVUMKUOgDcYxgZxz6KoyybaxXf3d%2Ftwc3adNtyk1NCUuT4oIh4%2FqSEt446oOlxfFw7tUXBKUicc%2Fh0dCkrlYk9xvFzv6UhFDxkol%2FxFZYX9sMCeF6yQY2FaWhP3sBq%2F7%2FpgDcORgyxgbOFmyY7bovl0Kkc9KFKY3xmYG11QprKTjCawet8iNHVhjwQta1r39TlHodaqNZ2GTGIwZUTbjoPj9W4UtFNTbNObSwJWG1h71wG83sm9mV61m6TSV4t4b2%2F1R7yGFnAJp%2FPgAF1Oumcq4u3cxq1XxLt%2BeblLPnbS5I0%2FTMDLLUNJwEuJrSPgxVVNMxbw6ttKrlY%2B%2B%2FXlJVytg6RQwE%2Bk78%2FhNoyDrHXjhLC%2BDpwVBLUSZAvCZm3N53Ri8GS%2FYonGsNabdibpja2wYXxBgC7oiBck4IgLuOKzIgFyZOxNjK2gS2W0w7o1MdF1VkYdw5VRpr4yGpxlZZSqrIz6Nq2ull2OjBT1R4NsKX8eXLbjWF6ZMsGreXrD1VCGuwVjxPnrag%2FwZWEDptoDXLAWiiR35BH0GUAiUl27jIIHNgHmZlOXOueC1ZTWX1MxCSxByurv2NIoxgZYi9jEoMZq6IuHdQkOAinr0l8mG1Mb21oN7tkOO2cU6S9cIeIbvciuKBmhlebMYNPTopwoQaCQXozJMmT3Lmupgf9jSZP0DE0pcA8kiqklF8rUqU9c1%2BIup1hcQfBuikycgWZfN%2F%2FTGx8OXO%2Bh9k66giRp4PW06nI0uRCDhf6rONg%2BPIv4PF5SQxhb5u%2FKJcc5j0Z77YGixMTiK4W8oCtoA%2FHswgTKWSSc59TlkEMWBwxya3VFUSc69ZjefsMzxCZbC9C8gQkyZa5ll35w1Vnbejgj4PYg%2FHv0OuHZkEOfqjE1wOpMxWQc69qd5huCqFDY8wvXlmUjMteBEFBN9QJIQu2YCH7mxXLMU41SPnFKO0G5skbAZwTtVC6g6ZZzE%2FSv1ULcHuSEUTT5XMK9RgGbQvcAB%2Fn6zcYTrSsCs%2FkBl4MuYaKLPb%2FCoF2H%2BRheDuIZv4Zk7iHN0c6u7w1u4U0lWfC0YTt47WeEgOki4FKYBBy7i%2BoNLiLwjra2Rq%2BZ8GKsgA%2FwjfOTsKjoUnfUIiF7umQ8nkO3Tcb3i4xLkPypZNwJ0R8s493D3Vp6G7gfRsY1AmUBe7LQU7u6JDy%2BcN4i4eg1OT8RO3ALGloXMTY5Gc%2B8Mi5R4DrVep6ispwsU5qm%2FUl7F8EAuIx0rBh6YE%2BYvtc71a3HNFUL9JGxxKsgCfDZOUoCd4TD9VVEo2QsnqiOqlDE6OxFnLoGC00rZL9H1e%2FU%2B4KmBwu4kKEAUYvHI1N1Fvmi8mLvAEkzUX0LpLIK8zru59iTvkMXzl126cQ3tIrv2nCKAcvtsksnNT2GN%2Bq9dKK6ucUfosSao%2Fye%2BPUzj%2FJljUc9a8g4dyqxN9oyoSqbUOG%2BHnOYUEWV4AkmVOH8iDsACPOcH91p5kcO9%2B8%2FP%2BIOuJzmbWJ8UaF6cUK6nBAER7rYQgKQ42QOSVTUnluEr4sWwNdTBOxuwYPYPGmELKoueuHRmFjl3kXEnv2DehcV7gFUfRCpF%2FbM%2BoMTBiYXRCJzACb3315KiUszuN8j8y2IFEaWSz73eORzS18EMrI9G96a2hYtMzEQKQfaf%2F9IiK502jvEugboWWDxO6vvvWhe3s6T%2FZq7OiUcLw7jLVxD7Yr3DFYH6KN4KQjpFtqopldkDLae%2BhEr6wYtfqrEko7jWsgrnR7oWC%2BLtSJ%2BY9ezKHhczRRVyO6ELPdyXruHs3RehfWq8V5ww4%2BxDFXv1duY921D6GiWEr%2BxEv9Urnd0fw5v2Zfuz8FeC4NnHa%2FjkJZdlrBhOkFkjwe1NsE8zhScXkN5sKlRHsjWRwhxpuj0uaG1kN28p50KEadB0dkJmWEbEtdgz7NQvZ5vWNTLTnhK5eyxtn0PsWC3UcPy1ofEfMuQmIvAq748DdBst1SIlOsP1Sd%2FfmddSNyzk3%2F7RqfYT308ausA1yV%2B4fZJ09BfDiKsHJgGC%2FGdGvYa6typKo%2BSu1dgkCEWPs9P36XnMkSO%2F632UlFJFiZluSJqruvdj%2FFCMsXBTPiPj%2FWx13%2F9mQ75M3xa7zPlyeJwSEWX6kbzPkgSGzz32mumWi28Sh%2Fnuvqvm97ymp%2FJLKX5ZNs51nwSic%2FA7xKcbBrZNrBtHGsbyJpHosZhqO2toZa3djyXIboaTza8UiR6zKIOXCnOsdvbW5HvypT3cEZF8AL7ybgX6NqJqMYKrTBCwdoilN3DaYUnNZ04uC0tknc56cBU7dIIjWe2%2BHEyUZOStwUgZ8YBFYZkPyQwnQmMqJDNHGBEoP27H4xoSKAuFSCLhc53vZMIkQ2BthnYjynVS2pRSll6yrd9wn2kap5pfl8ei5ugFC1eqsDf7nfBdoy%2FPQAu49dd%2Bjfehu8P4e5AwlaLpUsu%2BfiNi0vOXbKIKc60S9a3zHN6dSKTsseuVS8SGp%2BQ9S0LrLf7E6OuMSh9igRhODYse81kDYvwi9IxA7hlV8Afadr0eda3xOJjY%2FH%2BxMtKWiGRPPqfEDOB9SWChSZYP1JEkIxswGDkeu0ArNoAj7QPuEQArtF7gONQA%2BF94Y7Ue%2FFwqaO1%2BXCGZxDAYbx48ekrKmOcOJF14rxgrn0B0YHBih4f7oFtrsCGpJ3Xuzlhi2b%2FKkHOMZ9O6Kl23S3U%2BGR6pv0G7ZtPz3TxTs%2BhaXqkY9e6esp8oCpTd2MX3byntPHGnEEOQwEQZCD%2BgQ7FP3hHRAIpnfb0IyB6gxwUGB2ya5uskOomK%2FUKmuFdVhCeIS90qiKVQDbVleboobgWIulONZhXFJQj6SVLTbwK4%2BshpBIcdw9wkInFSCxab4AmVJNrSdGrlnIKZCAie9ecdXYqY8lnugKfyY%2BNjNUdQPnpetTyBtKjOXCDHo9ZSK7fXZ3yquXX6NeiPp8Km9Iu9t5xQU0RGC6UqqTWRKDWsI6hLhDgd17cmk631j0bO%2FN2gNT2LWegAyRwC7r0XpR%2Bcn%2BAh9PtC%2FmbVuQLD23fiztU4A59IlKLkr5Ts54RL55xFp5Rli9%2BIs%2Fo2INDw5pndFAaGk7nGTvx7b09Yy8itsUzij0jRVSkFtN5RhnO78Uz6veMsqDziTyjq9AzutN6xk7aII38lItbbHCLTpdbFCm7Rrcowzy%2BuEX9blGWBH0it8iQOrfI8KRusZOFqZdbjB%2FvwhPbFniGXjEjYGv1ioYLjMu6yTy8oj9vr%2Bgr9Ir%2BtF5R7WJLepe7aLe4xZFukXW5RbPBIhF4wakBGFXP9KNuzD2I60kROoN3s3SzBevpJ%2B%2FNFowgv3qOL2luJYED7Ba2YGUul8yHHVu4EV37PnSnCllKpt0YxlxrmONbDJf%2BAd1SponJiET9dW4YWgVTer1NzWYWKe%2BhU5vTTcMqybA6YW7ObSwVQ6M%2FlRtBZN5u%2Fyl%2B2cBy%2BmDwsiAD45pDfUEHnNlVFNJMX1Ei51PTD%2Fnlt%2F8ZQwm4JBU8iQC7FTIhP7ZhPZohlLtfRHCq8Y%2BqpMCTjXiQoa3wGNjyg0C6X0W0Uh4Wf09jHyWEiueIBc3JRb2e8480ZIprZtcRPgX7XWpq6YdDHKXGIzFSfSOegB7TE7gjGLIq42%2FG3aHp1D2nAzI0fX2qVMDCLHyxejiYu3tC69VWUFkjTI5zrnPvX4eCuFxdobbtjS49qtP2qLqs2h1XpacnVI71VUXHqlBLlDTR6wu3zjGkkigNeWYCpaYAZnig1Bz7QBY%2BCMfXvaxFJBZyF3%2Bp3196oMJO7HrIZ9RDdtJw9lrufNhn22893cWrZcmzp2LQqmJQVlcMUWlCm2KoRQdxxXiLF8Xopxg%2Bsi1S3YCZ%2BhPrhjcgilLJNdCX%2BFDANNAVvzTv6dMo0849e6RZjdTv2TNK3EKuZqgACwpM4ZqpWAzzhsYyRx0IjDmGQGCtL3qZ%2B2aGA2OoCwfG8yzVqzdiPVnQsbPwi%2FMGxzJXoV90J%2FWLarGxS7KozC86hvxi%2BjGOMiF%2BqlX6hp5%2Fj1ZhdsV%2FAA%3D%3D

