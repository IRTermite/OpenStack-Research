---


---

<blockquote>
<p>NOTE: THIS DOCUMENT IS UNDER CONSTRUCTION AND NOT COMPLETED OR VETTED.</p>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.<br>
Written by <a href="http://dale.bracey.come">Dale Bracey</a><br>
Expert Resource - Matt Heler<br>
Expert Resource - David Alfano</p>
</blockquote>
<h1 id="ceph-is-hard">CEPH is hard</h1>
<p>And understanding how it replicates data is hard.</p>
<blockquote>
<p>“How much free space do I leave to the CRUSH map for fault-tolerance on node failures?”<br>
“How many nodes can I lose and not lose data?”</p>
</blockquote>
<p>The following aims to help “over-simplify” the answers to those questions. In this example, we use a 5-node Ceph environment. The data distribution is also a simplified representation that simply explains the number of copies across nodes of each object; but, does not show it in a manner that depicts a large number of files/objects stored on the nodes.</p>
<p>Ceph also has a customizable …</p>
<p><strong>In this environment…</strong><br>
Pools = 1<br>
Placement Groups (PG) = 1<br>
OSDs (Disks) = ??<br>
Replicas = 3<br>
Objects = 5 (which just happen to all be of equal size and about a 1/4 the size of each node’s total available space)</p>
<p>Find more details at<br>
<a href="https://ceph.com/geen-categorie/how-data-is-stored-in-ceph-cluster/">https://ceph.com/geen-categorie/how-data-is-stored-in-ceph-cluster/</a></p>
<h2 id="healthy-ceph">Healthy CEPH</h2>
<p>Here, you will see the 5-node Ceph environment with its</p>
<p>CEPH with 5 Nodes (Healthy State)<br>
<img src="https://github.com/IRTermite/OpenStack-Research/blob/master/images/CEPHReplicationSimplified_HealthyState.png" alt="enter image description here"></p>
<h2 id="lost-a-node">Lost a Node</h2>
<p>CEPH with 5 Nodes (1 Node Failed)<br>
<img src="https://github.com/IRTermite/OpenStack-Research/blob/master/images/CEPHReplicationSimplified_1-NodeFailure.png" alt="enter image description here"></p>
<h2 id="can-i-lose-another-node">Can I lose another node?</h2>
<p>CEPH with 5 Nodes (2 Nodes Failed)<br>
<img src="https://github.com/IRTermite/OpenStack-Research/blob/master/images/CEPHReplicationSimplified_2-NodeFailure.png" alt="enter image description here"></p>

