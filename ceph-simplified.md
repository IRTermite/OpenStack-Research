---


---

<blockquote>
<p>NOTE: THIS DOCUMENT IS UNDER CONSTRUCTION AND NOT COMPLETED OR VETTED.</p>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>
<p>CEPH is hard. And understanding how it replicates data is hard.</p>
<blockquote>
<p>“How much free space to I leave to the CRUSH map for fault-tolerance on node failures?”<br>
“How many nodes can I lose and not lose data?”</p>
</blockquote>
<p>The following aims to help “over-simplify” the answers to those questions.</p>
<p>CEPH with 5 Nodes (Healthy State)<br>
<img src="https://github.com/IRTermite/OpenStack-Research/blob/master/images/CEPHReplicationSimplified_HealthyState.png" alt="enter image description here"></p>
<p>CEPH with 5 Nodes (1 Node Failed)<br>
<img src="https://github.com/IRTermite/OpenStack-Research/blob/master/images/CEPHReplicationSimplified_1-NodeFailure.png" alt="enter image description here"></p>
<p>CEPH with 5 Nodes (2 Nodes Failed)<br>
<img src="https://github.com/IRTermite/OpenStack-Research/blob/master/images/CEPHReplicationSimplified_2-NodeFailure.png" alt="enter image description here"></p>

