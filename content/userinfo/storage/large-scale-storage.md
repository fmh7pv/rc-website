+++
author = "SOMRC Staff"
description = ""
title = "Large-Scale Research Data Storage"
date = "2018-04-19T10:08:29-05:00"
draft = false
tags = ["storage","large scale"]
categories = ["userinfo"]
images = [""]
+++


<p class="lead">There are a variety of options for storing large-scale research data at UVa. Non-sensitive data storage systems can be accessed from the <a href="https://arcs.virginia.edu/rivanna" target="_blank">Rivanna</a> high performance computing system. Sensitive data can be stored and accessed within the <a href="/userinfo/ivy">Ivy</a> secure computing environment.</p>
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;border-color:#ccc;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-color:#ccc;color:#333;background-color:#fff;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-color:#ccc;color:#333;background-color:#f0f0f0;}
.tg .tg-hy9w{background-color:#eceeef;border-color:inherit;vertical-align:top}
.tg .tg-dc35{background-color:#f9f9f9;border-color:inherit;vertical-align:top}
.tg .tg-0qmj{font-weight:bold;background-color:#eceeef;border-color:inherit;vertical-align:top}
</style>
<div>
<h3>Non-Sensitive Data Storage</h3>
<table class="tg">
  <tr>
    <th class="tg-0qmj">Name</th>
    <th class="tg-0qmj">Quota</th>
    <th class="tg-0qmj">Price</th>
    <th class="tg-0qmj">Data Protection</th>
    <!-- <th class="tg-0qmj">File system</th> -->
    <th class="tg-0qmj">Accessible from</th>
    <th class="tg-0qmj">Best Practices</th>
  </tr>
  <tr>
    <td class="tg-dc35"><a href="/userinfo/storage/non-sensitive-data/#home"><code>/home</code></a></td>
    <td class="tg-dc35">50GB</td>
    <td class="tg-dc35">Free</td>
    <td class="tg-dc35">3-week snapshot</td>
    <!-- <td class="tg-dc35">NFS</td> -->
    <td class="tg-dc35">Rivanna login and compute nodes</td>
    <td class="tg-dc35"><code>/home</code> is best used as a working directory when using Rivanna interactively. SLURM jobs run against <code>/home</code> will be slower than those run against <code>/scratch</code>.</td>
  </tr>
  <tr>
    <td class="tg-hy9w"><a href="/userinfo/storage/non-sensitive-data/#scratch"><code>/scratch</code></a></td>
    <td class="tg-hy9w">10TB</td>
    <td class="tg-hy9w">Free</td>
    <td class="tg-hy9w">Data removed 60 days after last file modification timestamp</td>
    <!-- <td class="tg-hy9w">Lustre</td> -->
    <td class="tg-hy9w">Rivanna login and compute nodes</td>
    <td class="tg-hy9w"><code>/scratch</code> is a high performance parallel filesystem that is suitable for large scale computational work. Data should be moved from <code>/scratch</code> for long-term storage.</td>
  </tr>
  <tr>
    <td class="tg-dc35"><a href="/userinfo/storage/non-sensitive-data/#project"><code>/project</code></a></td> 
    <td class="tg-dc35">Available in 1TB increments</td>
    <td class="tg-dc35">$90/TB/Yr</td>
    <td class="tg-dc35">3-week snapshot</td>
    <!-- <td class="tg-dc35">NFS</td> -->
    <td class="tg-dc35">Rivanna login and compute nodes</td>
    <td class="tg-dc35"><code>/project</code>is ideal for long-term storage of data that can be accessed from Rivanna. <code>/project</code> is ideal for running jobs with smaller files.</td>
  </tr>
  <tr>
    <td class="tg-hy9w"><a href="/userinfo/storage/research-value">Value Storage</a></td>  
    <td class="tg-hy9w">Available in 1TB increments</td>
    <td class="tg-hy9w">$45/TB/Yr</td>
    <td class="tg-hy9w">No backup</td>
    <!-- <td class="tg-hy9w">Proprietary</td> -->
    <td class="tg-hy9w">Rivanna login and compute nodes, SMB mount</td>
    <td class="tg-hy9w">Research value storage budget solution for storing data that can be accessed by a personal computer or Rivanna. SLURM jobs can be run against value storage but will be slower than those run against <code>/home</code>, <code>/scratch</code>, or <code>/project</code>.</td>
  </tr>
</table>
</div>
<br>

<div>
<h3>Sensitive Data Storage</h3>
<table class="tg">
	<tr>
		<th class="tg-0qmj">Name</th>
		<th class="tg-0qmj">Quota</th>
		<th class="tg-0qmj">Price</th>
		<!--<th class="tg-0qmj">Data Protection</th>
		<th class="tg-0qmj">File System</th> -->
		<th class="tg-0qmj">Mounted On</th>
		<th class="tg-0qmj">Best Practices</th>
	</tr>
	<tr>
		<td class="tg-dc35"><a href="/userinfo/storage/sensitive-data/#ivy-central-storage">Ivy Central Storage (ICS)</a></td>
		<td class="tg-dc35">Available in 1TB increments</td>
		<td class="tg-dc35">First TB is free, price for additional space TBD</td>
		<!-- <td class="tg-dc35">No backup</td>
		<td class="tg-dc35"></td> -->
		<td class="tg-dc35">Ivy virtual machine</td>
		<td class="tg-dc35">ICS is ideal for long-term storage of sensitive data and is suitable for computation with smaller file sizes. Files stored in ICS are read-write only.</td>
	</tr>
	<tr>
		<td class="tg-hy9w"><a href="/userinfo/storage/sensitive-data/#vm-storage">VM Storage</a></td>
		<td class="tg-hy9w">Available in 1TB increments</td>
		<td class="tg-hy9w">First TB is free, price for additional space TBD</td>
		<!-- <td class="tg-hy9w">No backup</td>
		<td class="tg-hy9w"></td> -->
		<td class="tg-hy9w">Ivy virtual machine</td>
		<td class="tg-hy9w">VM Storage is suitable for storing executables and jobs that require higher I/O performance than that provided by ICS.</td>
	</tr>
	<tr>
		<td class="tg-dc35"><a href="/userinfo/storage/sensitive-data/#ddl-storage">DDL Storage</a></td>
		<td class="tg-dc35">500GB per project</td>
		<td class="tg-dc35">Currently free, price TBD</td>
		<!-- <td class="tg-dc35"></td>
		<td class="tg-dc35"></td> -->
		<td class="tg-dc35">Domino Data Lab</td>
		<td class="tg-dc35">This storage type is available for data science projects managed with Domino Data Lab.</td>
	</tr>
</table>
</div>