# KDR

Data races are increasingly seen as concurrency bugs and they are difficult to reproduce and diagnose in parallel programs. Linux kernel is a concurrency-intensive and large-scale software system that contains million lines of code contributed by more than 10 thousands programmers. High thread-level parallelism and non-deterministic thread interleaving are most prone to race conditions. We conducted a thorough investigation of data races reported on Linux kernels in recent 5 years. The investigation was performed by reviewing bug reports in Kernel Bug Tracker and studying kernel source code revision logs in Linux Kernel Organization. The results show that there are about 500 kernel data races reported and fixed in recent 5 years, and the file system and drivers among all modules have a much higher percentage of race conditions than other modules. Race distribution over years, modules and kernel versions are also reported according to our statistical results. We conducted a case-by-case study on some selected data races and summed up 4 data race patterns. Our analysis results should be of interest to researchers and engineers who are committed to kernel data race detection and kernel development.


<br>
<br>

If this is useful for you, please cite our paper:
Shi, Jianjun & Ji, Weixing & Wang, Yizhuo & Huang, Lifu & Guo, Yunkun & Shi, Feng. (2018). <b>Linux Kernel Data Races in Recent 5 Years</b>. Chinese Journal of Electronics. 27. 556-560. 10.1049/cje.2018.03.015. 

<!--h2>Contact information: </h2>
<table>
<tr><td>
  Jianjun Shi (Beijing Institute of Technology) 
<tr><td>
  Weixing Ji (Beijing Institute of Technology) &lt;jwx@bit.edu.cn&gt;
</table-->
  
<h2>References:</h2>
<table>
<tr><td>
[1]<a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/"> Kernel.org git repositories </a>
<tr><td>
[2]<a href="https://www.kernel.org">The Linux Kernel Archives</a>

</table>

<table>
    <tr> <th> list                      <th> source          <th> module         <th> version       <th> id     <th> status   
    <tr background="red";> <td> [<a href="#c1">1</a>]     <td> ChangeLog      <td> IO         <td> 3.10.8     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=d50235b7bc3ee0a0427984d763ea7534149531b4">d50235b7bc3ee0a0427984d763ea7534149531b4</a>    <td> Resolved
    <tr> <td> [<a href="#c2">2</a>]     <td> ChangeLog      <td> Driver         <td> 3.0.38     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=8265981bb439f3ecc5356fb877a6c2a6636ac88a">8265981bb439f3ecc5356fb877a6c2a6636ac88a</a>    <td> Resolved
    <tr> <td> [<a href="#c3">3</a>]     <td> ChangeLog      <td> Driver         <td> 3.0.59     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=ce73ec6db47af84d1466402781ae0872a9e7873c">ce73ec6db47af84d1466402781ae0872a9e7873c</a>    <td> Resolved
    <tr> <td> [<a href="#c4">4</a>]     <td> ChangeLog      <td> KVM         <td> 3.10.60     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=2febc839133280d5a5e8e1179c94ea674489dae2">2febc839133280d5a5e8e1179c94ea674489dae2</a>    <td> Resolved
    <tr> <td> [<a href="#c5">5</a>]     <td> ChangeLog      <td> KVM         <td> 3.3.6     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=6dbf79e7164e9a86c1e466062c48498142ae6128">6dbf79e7164e9a86c1e466062c48498142ae6128</a>    <td> Resolved
    <tr> <td> [<a href="#c6">6</a>]     <td> ChangeLog      <td> IO         <td> 3.10.23    
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=eb1c160b22655fd4ec44be732d6594fd1b1e44f4">eb1c160b22655fd4ec44be732d6594fd1b1e44f4</a>    <td> Resolved
    <tr> <td> [<a href="#c7">7</a>]  	<td> ChangeLog 	<td> Driver             	<td> 3.1     	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=9c921c22a7f33397a6774d7fa076db9b6a0fd669">9c921c22a7f33397a6774d7fa076db9b6a0fd669 	<td> Resolved 	
 <tr> <td> [<a href="#c8">8</a>]  	<td> ChangeLog 	<td> Driver             	<td> 3.1     	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=7456caae37396fc1bc6f8e9461d07664b8c2f280">7456caae37396fc1bc6f8e9461d07664b8c2f280 	<td> Resolved 	
<tr> <td> [<a href="#c9">9</a>]   	<td> ChangeLog <td> Driver            <td> 3.0.11  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=5dc2470c602da8851907ec18942cd876c3b4ecc1">5dc2470c602da8851907ec18942cd876c3b4ecc1 	<td> Resolved 	
<tr> <td> [<a href="#c10">10</a>]  	<td> ChangeLog 	<td>Driver             	<td> 3.0.17  <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=eea915bb0d1358755f151eaefb8208a2d5f3e10c
">eea915bb0d1358755f151eaefb8208a2d5f3e10c 	<td> Resolved 
<tr> <td> [<a href="#c11">11</a>]  	<td>ChangeLog <td> Driver             <td> 3.0.41  <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=44e4360fa3384850d65dd36fb4e6e5f2f112709b">44e4360fa3384850d65dd36fb4e6e5f2f112709b 	<td> Resolved 	
<tr> <td> [<a href="#c12">12</a>]  	<td> ChangeLog 	<td> Driver             	<td> 3.11.2  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=1eeeef153c02f5856ec109fa532eb5f31c39f85c">1eeeef153c02f5856ec109fa532eb5f31c39f85c 	<td>Resolved 	
<tr> <td> [<a href="#c13">13</a>]  	<td> ChangeLog <td> Driver             	<td> 3.10.34 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=ef0899410ff630b2e75306da49996dbbfa318165">ef0899410ff630b2e75306da49996dbbfa318165 	<td>Resolved 
<tr> <td> [<a href="#c14">14</a>]  	<td> ChangeLog 	<td>Driver             	<td> 3.10.23 <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=b869ccfab1e324507fa3596e3e1308444fb68227">b869ccfab1e324507fa3596e3e1308444fb68227 	<td>Resolved 
<tr> <td> [<a href="#c15">15</a>]  <td> ChangeLog <td> Driver             <td> 3.10.42 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=21f8aaee0c62708654988ce092838aa7df4d25d8">21f8aaee0c62708654988ce092838aa7df4d25d8 	<td> Resolved 	
<tr> <td> [<a href="#c16">16</a>]  	<td> ChangeLog 	<td> Driver             <td> 3.10.46 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=d9e93c08d8d985e5ef89436ebc9f4aad7e31559f">d9e93c08d8d985e5ef89436ebc9f4aad7e31559f 	<td> Resolved 
<tr> <td> [<a href="#c17">17</a>]  	<td> ChangeLog <td>File System        <td> 3.10.39 <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=ec4cb1aa2b7bae18dd8164f2e9c7c51abcf61280">ec4cb1aa2b7bae18dd8164f2e9c7c51abcf61280 	<td> Resolved 	
<tr> <td> [<a href="#c18">18</a>]  	<td> ChangeLog 	<td> File System        <td> 3.2.45  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=794446c6946513c684d448205fbd76fa35f38b72">794446c6946513c684d448205fbd76fa35f38b72 	<td> Resolved 
<tr> <td> [<a href="#c19">19</a>]  	<td> ChangeLog <td> File System        	<td> 3.10.66 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=06bed7d18c2c07b3e3eeadf4bd357f6e806618cc">06bed7d18c2c07b3e3eeadf4bd357f6e806618cc 	<td> Resolved 
<tr> <td> [<a href="#c20">20</a>]  	<td> ChangeLog 	<td> File System        <td> 3.0.88  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=1c327d962fc420aea046c16215a552710bde8231">1c327d962fc420aea046c16215a552710bde8231 	<td> Resolved 	
<tr> <td> [<a href="#c21">21</a>]  	<td> ChangeLog 	<td> Process Management 	<td> 3.0.68  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=71b5707e119653039e6e95213f00479668c79b75">71b5707e119653039e6e95213f00479668c79b75 	<td> Resolved 
<tr> <td> [<a href="#c22">22</a>]  	<td> ChangeLog 	<td> Process Management <td> 3.12.14 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=532de3fc72adc2a6525c4d53c07bf81e1732083d">532de3fc72adc2a6525c4d53c07bf81e1732083d 	<td> Resolved 
<tr> <td> [<a href="#c23">23</a>]  	<td> ChangeLog 	<td> Process Management 	<td> 3.12.37 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=c291ee622165cb2c8d4e7af63fffd499354a23be">c291ee622165cb2c8d4e7af63fffd499354a23be 	<td> Resolved 
<tr> <td> [<a href="#c24">24</a>]  	<td> ChangeLog 	<td>Process Management <td> 3.14.41 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=b72c186999e689cb0b055ab1c7b3cd8fffbeb5ed">b72c186999e689cb0b055ab1c7b3cd8fffbeb5ed 	<td> Resolved 
<tr> <td> [<a href="#c25">25</a>]  <td> ChangeLog 	<td> Memory Management  	<td> 3.12.36 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=91b57191cfd152c02ded0745250167d0263084f8">91b57191cfd152c02ded0745250167d0263084f8 	<td> Resolved 	
<tr> <td> [<a href="#c26">26</a>]  <td> ChangeLog 	<td> File System  	<td> 3.10.33 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=1362f4ea20fa63688ba6026e586d9746ff13a846
">1362f4ea20fa63688ba6026e586d9746ff13a846
 	<td> Resolved     
 	<tr> <td> [<a href="#c27">27</a>]  	<td> ChangeLog 	<td> Drivers 	<td> 3.7.2  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=bd9eb7fbe69111ea0ff1f999ef4a5f26d223d1d5">bd9eb7fbe69111ea0ff1f999ef4a5f26d223d1d5 	<td> Resolved 
<tr> <td> [<a href="#c28">28</a>]  	<td> ChangeLog 	<td>Process Management <td> 3.10.21 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=a399b29dfbaaaf91162b2dc5a5875dd51bbfa2a1">a399b29dfbaaaf91162b2dc5a5875dd51bbfa2a1 	<td> Resolved 
<tr> <td> [<a href="#c29">29</a>]  <td> ChangeLog 	<td> File System  	<td> 3.10.62 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=c6c15e1ed303ffc47e696ea1c9a9df1761c1f603">c6c15e1ed303ffc47e696ea1c9a9df1761c1f603 	<td> Resolved 	
<tr> <td> [<a href="#c30">30</a>]  <td> ChangeLog 	<td> Others  	<td> 3.17.3 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=30a6b8031fe14031ab27c1fa3483cb9780e7f63c
">30a6b8031fe14031ab27c1fa3483cb9780e7f63c
 	<td> Resolved     
</table>

<table>
     <tr><td colspan="4"> <h4> #1 </h4>
    <tr><th> <a name="c1" id="c1"></a> Commit id <td>d50235b7bc3ee0a0427984d763ea7534149531b4
        <th>Version      <td>3.10.8    
    <tr><th>Module      <td>IO           <th>Date                <td>2013/7/3
    <tr> <th>Pattern             <td colspan="3">use before initialization   
    <tr> <th>Description <td colspan="3">There's a race between elevator switching and normal io operation.
    Because the allocation of struct elevator_queue and struct elevator_data
    don't in a atomic operation.So there are have chance to use NULL
    ->elevator_data.
    <tr> <th>Reproduce   <td colspan="3">Using the follow method can easy reproduce this bug
    1:dd if=/dev/sdb of=/dev/null
    2:while true;do echo noop > scheduler;echo deadline > scheduler;done
    <tr><th>Interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/4531815/8325292/c77a173e-1a8a-11e5-9ddd-7f7b8a3ac0a5.png"></table>
      
<table>
    <tr><td colspan="4"> <h4> #2 </h4>
    <tr><th> <a name="c2" id="c2"></a> commit id <td>8265981bb439f3ecc5356fb877a6c2a6636ac88a
        <th>kernel version      <td>3.0.38    
    <tr><th>module      <td>Driver           <th>date                <td>2012/7/13
    <tr> <th>pattern             <td colspan="3">access with improper synchronization  
    <tr> <th> description <td colspan="3">Checking for adc->ts_pend already claimed should be done with the
lock held.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8777996/e5301c6c-2f2d-11e5-9c20-b5067b0ac989.png"></table>
    
<table>
    <tr><td colspan="4"> <h4> #3 </h4>
    <tr><th> <a name="c3" id="c3"></a> commit id <td>ce73ec6db47af84d1466402781ae0872a9e7873c
        <th>kernel version      <td>3.0.38    
    <tr><th>module      <td>Driver           <th>date                <td>2013/1/3
    <tr> <th>pattern             <td colspan="3">access with improper synchronization   
    <tr> <th> description <td colspan="3">The locking in update_vsyscall_tz() is not only unnecessary because the vdso
code copies the data unproteced in __kernel_gettimeofday() but also
introduces a hard to reproduce race condition between update_vsyscall()
and update_vsyscall_tz(), which causes user space process to loop
forever in vdso code.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8778028/14832356-2f2e-11e5-8542-ed5b210cd26e.png">
</table>  
      
<table>
     <tr><td colspan="4"> <h4> #4 </h4>
    <tr><th> <a name="c4" id="c4"></a> commit id <td>2febc839133280d5a5e8e1179c94ea674489dae2
        <th>kernel version      <td>3.10.60    
    <tr><th>module      <td>KVM           <th>date                <td>2014/10/24
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">There's a race condition in the PIT emulation code in KVM.  In
__kvm_migrate_pit_timer the pit_timer object is accessed without
synchronization.  If the race condition occurs at the wrong time this
can crash the host kernel.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8778034/247a667a-2f2e-11e5-9ef6-a831beb2591b.png">
</table>
<table>    
     <tr><td colspan="4"> <h4> #5 </h4>
    <tr><th> <a name="c5" id="c5"></a> commit id <td>6dbf79e7164e9a86c1e466062c48498142ae6128
        <th>kernel version      <td>3.3.6    
    <tr><th>module      <td>KVM           <th>date                <td>2012/3/8
    <tr> <th>pattern             <td colspan="3">access with improper synchronization   
    <tr> <th> description <td colspan="3">During protecting pages for dirty logging, other threads may also try
to protect a page in mmu_sync_children() or kvm_mmu_get_page().
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8778041/2e47b568-2f2e-11e5-8cc8-83f16878dab1.png">
</table>    
<table>    
     <tr><td colspan="4"> <h4> #6 </h4>
    <tr><th> <a name="c6" id="c6"></a> commit id <td>eb1c160b22655fd4ec44be732d6594fd1b1e44f4
        <th>kernel version      <td>3.10.23    
    <tr><th>module      <td>IO           <th>date                <td>2013/11/8
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">The soft lockup below happens at the boot time of the system using dm
multipath and the udev rules to switch scheduler.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795136/c391b9a0-2fbc-11e5-9960-ba8287a19a15.png">
</table>
<table>
     <tr><td colspan="4"> <h4> #7 </h4>
    <tr><th> <a name="c7" id="c7"></a> commit id <td>9c921c22a7f33397a6774d7fa076db9b6a0fd669
        <th>kernel version      <td>3.1   
    <tr><th>module      <td>Driver           <th>date                <td>2011/7/14
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">Use battery->lock in sysfs_remove_battery() to make
checking, removing, and clearing bat.dev atomic.
This is necessary because sysfs_remove_battery() may
be invoked concurrently from different paths.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795140/d09599a0-2fbc-11e5-940c-9e417a413bd0.png">
</table>
<table>
     <tr><td colspan="4"> <h4> #8 </h4>
    <tr><th> <a name="c8" id="c8"></a> commit id <td>7456caae37396fc1bc6f8e9461d07664b8c2f280
        <th>kernel version      <td>3.1   
    <tr><th>module      <td>Driver           <th>date                <td>2011/7/20
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">When a request is made, the card presence is checked and the request is
queued. These two parts must be atomic with respect to card removal, or
a card removal could be handled in between, and the new request wouldn't
get cancelled until another card was inserted.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795143/d6550ee8-2fbc-11e5-98b0-2ee1b2db0db0.png">
</table>
<table>      
     <tr><td colspan="4"> <h4> #9 </h4>
    <tr><th> <a name="c9" id="c9"></a> commit id <td>5dc2470c602da8851907ec18942cd876c3b4ecc1
        <th>kernel version      <td>3.0.11   
    <tr><th>module      <td>Driver           <th>date                <td>2011/11/14
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">There's a race between the USB disconnect handler and the TTY close
handler which may cause the acm object to be freed while it's still
being used. 
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795150/e9cf161c-2fbc-11e5-8d17-53a45a4b7fcb.png">
</table>
<table>      
     <tr><td colspan="4"> <h4> #10 </h4>
    <tr><th> <a name="c10" id="c10"></a> commit id <td>eea915bb0d1358755f151eaefb8208a2d5f3e10c
        <th>kernel version      <td>3.0.17   
    <tr><th>module      <td>Driver           <th>date                <td>2012/1/5
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">Its caused by the fact that firmware_loading_store has a case 0 in its
switch statement that reads and writes the fw_priv->fw poniter without the
protection of the fw_lock mutex. 
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795197/69d2aee6-2fbd-11e5-84f0-35d94945859a.png">
</table>
<table>      
     <tr><td colspan="4"> <h4> #11 </h4>
    <tr><th> <a name="c11" id="c11"></a> commit id <td>44e4360fa3384850d65dd36fb4e6e5f2f112709b
        <th>kernel version      <td>3.0.41   
    <tr><th>module      <td>Driver           <th>date                <td>2012/4/12
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">/proc/sys/kernel/random/boot_id can be read concurrently by userspace
processes.  If two (or more) user-space processes concurrently read
boot_id when sysctl_bootid is not yet assigned, a race can occur making
boot_id differ between the reads. 
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795212/8f93c098-2fbd-11e5-88d6-1427c7cd6a10.png">
</table>
<table>      
     <tr><td colspan="4"> <h4> #12 </h4>
    <tr><th> <a name="c12" id="c12"></a> commit id <td>1eeeef153c02f5856ec109fa532eb5f31c39f85c
        <th>kernel version      <td>3.11.2   
    <tr><th>module      <td>Driver           <th>date                <td>2013/8/30
    <tr> <th>pattern             <td colspan="3">use after free   
    <tr> <th> description <td colspan="3">The following race condition triggers here.
causing an oops later when walking pending_list after the firmware has
been released.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795216/a3df670a-2fbd-11e5-85dd-ec9ed62b8db4.png">
</table>
<table>      
     <tr><td colspan="4"> <h4> #13 </h4>
    <tr><th> <a name="c13" id="c13"></a> commit id <td>ef0899410ff630b2e75306da49996dbbfa318165
        <th>kernel version      <td>3.10.34  
    <tr><th>module      <td>Driver           <th>date                <td>2013/11/8
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">The patch did not convert the s390 dasd device driver which is the only
device driver which also calls elevator_init(). So add the missing locking.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8800605/ca47906a-2fe6-11e5-84a3-282735902e56.png">
</table> 
<table>      
     <tr><td colspan="4"> <h4> #14 </h4>
    <tr><th> <a name="c14" id="c14"></a> commit id <td>b869ccfab1e324507fa3596e3e1308444fb68227
        <th>kernel version      <td>3.10.23   
    <tr><th>module      <td>Driver           <th>date                <td>2013/11/14
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">This patch fixes two race conditions between bond_store_updelay/downdelay
and bond_store_miimon which could lead to division by zero as miimon can
be set to 0 while either updelay/downdelay are being set and thus miss the
zero check in the beginning, the zero div happens because updelay/downdelay
are stored as new_value / bond->params.miimon. Use rtnl to synchronize with
miimon setting.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795372/341b7b96-2fbf-11e5-9dee-6cc5a981a969.png">
</table> 
<table>      
     <tr><td colspan="4"> <h4> #15 </h4>
    <tr><th> <a name="c15" id="c15"></a> commit id <td>21f8aaee0c62708654988ce092838aa7df4d25d8
        <th>kernel version      <td>3.10.42   
    <tr><th>module      <td>Driver           <th>date                <td>2014/2/20
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">We check tid->sched without a lock taken on ath_tx_aggr_sleep(). That
is race condition which can result of doing list_del(&tid->list) twice
(second time with poisoned list node) and cause crash like shown below:
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795382/3cc4a510-2fbf-11e5-8f63-d3285b5665de.png">
</table>
<table>      
     <tr><td colspan="4"> <h4> #16 </h4>
    <tr><th> <a name="c16" id="c16"></a> commit id <td>d9e93c08d8d985e5ef89436ebc9f4aad7e31559f
        <th>kernel version      <td>3.10.46   
    <tr><th>module      <td>Driver           <th>date                <td>2014/5/27
    <tr> <th>pattern             <td colspan="3">access with improper synchronization   
    <tr> <th> description <td colspan="3">We find a race between write and resume. usb_wwan_resume run play_delayed()
and spin_unlock, but intfdata->suspended still is not set to zero.
At this time usb_wwan_write is called and anchor the urb to delay
list. Then resume keep running but the delayed urb have no chance
to be commit until next resume. If the time of next resume is far
away, tty will be blocked in tty_wait_until_sent during time. The
race also can lead to writes being reordered.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795400/5ff7d1e2-2fbf-11e5-9266-d7c32fafc290.png">
</table>
<table>      
     <tr><td colspan="4"> <h4> #17 </h4>
    <tr><th> <a name="c17" id="c17"></a> commit id <td>ec4cb1aa2b7bae18dd8164f2e9c7c51abcf61280
        <th>kernel version      <td>3.10.39   
    <tr><th>module      <td>File System           <th>date                <td>2014/4/7
    <tr> <th>pattern             <td colspan="3">access with improper synchronization   
    <tr> <th> description <td colspan="3">When heavily exercising xattr code the assertion that
jbd2_journal_dirty_metadata() shouldn't return error was triggered.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795406/6d8fc63e-2fbf-11e5-8111-03aadf62a10f.png">
</table>
<table>      
      <tr><td colspan="4"> <h4> #18 </h4>
    <tr><th> <a name="c18" id="c18"></a> commit id <td>794446c6946513c684d448205fbd76fa35f38b72
        <th>kernel version      <td>3.2.45   
    <tr><th>module      <td>File System           <th>date                <td>2013/4/4
    <tr> <th>pattern             <td colspan="3">use after free   
    <tr> <th> description <td colspan="3">In order to demonstrace this issue one should mount ext4 with mount -o
discard option on SSD disk.  This makes callback longer and race
window becomes wider.
In order to fix this we should mark transaction as finished only after
callbacks have completed
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8800613/d683fabc-2fe6-11e5-8ed5-644cc9633523.png">
</table>
<table>      
     <tr><td colspan="4"> <h4> #19 </h4>
    <tr><th> <a name="c19" id="c19"></a> commit id <td>06bed7d18c2c07b3e3eeadf4bd357f6e806618cc
        <th>kernel version      <td>3.10.39   
    <tr><th>module      <td>File System           <th>date                <td>2014/4/7
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">This commit fixes a race whereby nlmclnt_init() first starts the lockd
daemon, and then calls nlm_bind_host() with the expectation that
nlmsvc_timeout has already been initialised. Unfortunately, there is no
no synchronisation between lockd() and lockd_up() to guarantee that this
is the case.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://raw.githubusercontent.com/BIT-SYS/KDR/master/Images/06bed7d18c2c07b3e3eeadf4bd357f6e806618cc.png">
</table>
<table>
     <tr><td colspan="4"> <h4> #20 </h4>
    <tr><th> <a name="c20" id="c20"></a> commit id <td>1c327d962fc420aea046c16215a552710bde8231
        <th>kernel version      <td>3.0.88   
    <tr><th>module      <td>File System           <th>date                <td>2013/7/11
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">In nlmsvc_retry_blocked, the check that the list is non-empty and acquiring
the pointer of the first entry is unprotected by any lock.  This allows a rare
race condition when there is only one entry on the list.  A function such as
nlmsvc_grant_callback() can be called, which will temporarily remove the entry
from the list.  Between the list_empty() and list_entry(),the list may become
empty, causing an invalid pointer to be used as an nlm_block, leading to a
possible crash.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8815619/30e55002-304e-11e5-8b41-b7c514ed05b1.png">
</table>   
<table>      
     <tr><td colspan="4"> <h4> #21 </h4>
    <tr><th> <a name="c21" id="c21"></a> commit id <td>71b5707e119653039e6e95213f00479668c79b75
        <th>kernel version      <td>3.0.68   
    <tr><th>module      <td>Process Management           <th>date                <td>2013/2/18
    <tr> <th>pattern             <td colspan="3">use after free   
    <tr> <th> description <td colspan="3">In cgroup_exit() put_css_set_taskexit() is called without any lock,
which might lead to accessing a freed cgroup.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8800211/8154ab66-2fe3-11e5-8f22-3e5ba0f18d6e.png">
</table>
<table>      
      <tr><td colspan="4"> <h4> #22 </h4>
    <tr><th> <a name="c22" id="c22"></a> commit id <td>532de3fc72adc2a6525c4d53c07bf81e1732083d
        <th>kernel version      <td>3.12.14   
    <tr><th>module      <td>Process Management           <th>date                <td>2014/2/18
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">Currently, there's nothing preventing cgroup_enable_task_cg_lists()
from missing set PF_EXITING and race against cgroup_exit().  Depending
on the timing, cgroup_exit() may finish with the task still linked on
css_set leading to list corruption.  Fix it by grabbing siglock in
cgroup_enable_task_cg_lists() so that PF_EXITING is guaranteed to be
visible.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8815623/380996a4-304e-11e5-9a97-e394bbbfc1d6.png">
</table>
 <table>     
      <tr><td colspan="4"> <h4> #23 </h4>
    <tr><th> <a name="c23" id="c23"></a> commit id <td>c291ee622165cb2c8d4e7af63fffd499354a23be
        <th>kernel version      <td>3.12.37   
    <tr><th>module      <td>Process Management           <th>date                <td>2014/12/13
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">Since the rework of the sparse interrupt code to actually free the
unused interrupt descriptors there exists a race between the /proc
interfaces to the irq subsystem and the code which frees the interrupt
descriptor.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8800220/8c970aaa-2fe3-11e5-9040-6cd6358d770b.png">
</table>
<table>      
      <tr><td colspan="4"> <h4> #24 </h4>
    <tr><th> <a name="c24" id="c24"></a> commit id <td>b72c186999e689cb0b055ab1c7b3cd8fffbeb5ed
        <th>kernel version      <td>3.14.41   
    <tr><th>module      <td>Process Management           <th>date                <td>2015/4/17
    <tr> <th>pattern             <td colspan="3">use after free   
    <tr> <th> description <td colspan="3">ptrace_resume() is called when the tracee is still __TASK_TRACED.  We set
tracee->exit_code and then wake_up_state() changes tracee->state.  If the
tracer's sub-thread does wait() in between, task_stopped_code(ptrace => T)
wrongly looks like another report from tracee.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8800224/97412a6c-2fe3-11e5-942e-7dd4f0b1709a.png">
</table>
<table>      
      <tr><td colspan="4"> <h4> #25 </h4>
    <tr><th> <a name="c25" id="c25"></a> commit id <td>91b57191cfd152c02ded0745250167d0263084f8
        <th>kernel version      <td>3.12.36   
    <tr><th>module      <td>Memory Management           <th>date                <td>2014/12/3
    <tr> <th>pattern             <td colspan="3">access with improper synchronization   
    <tr> <th> description <td colspan="3">In some android devices, there will be a "divide by zero" exception.
vmpr->scanned could be zero before spin_lock(&vmpr->sr_lock).
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8800265/e9c924ce-2fe3-11e5-961e-68d4585cf701.png">
</table>
<table>      
       <tr><td colspan="4"> <h4> #26 </h4>
    <tr><th> <a name="c26" id="c26"></a> commit id <td>1362f4ea20fa63688ba6026e586d9746ff13a846
        <th>kernel version      <td>3.14.41   
    <tr><th>module      <td>File System           <th>date                <td>2014/2/20
    <tr> <th>pattern             <td colspan="3">use after free   
    <tr> <th> description <td colspan="3">Currently last dqput() can race with dquot_scan_active() causing it to
call callback for an already deactivated dquot.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8828786/88d05690-30c6-11e5-96e8-2699432e18d7.png">
</table>
<table>      
       <tr><td colspan="4"> <h4> #27 </h4>
    <tr><th> <a name="c27" id="c27"></a> commit id <td>bd9eb7fbe69111ea0ff1f999ef4a5f26d223d1d5
        <th>kernel version      <td>3.7.2   
    <tr><th>module      <td>Drivers           <th>date                <td>2012/11/14
    <tr> <th>pattern             <td colspan="3">use after free   
    <tr> <th> description <td colspan="3">There is one race that both request_firmware() with the same
firmware name.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8828812/9d6061e0-30c6-11e5-9a77-d8e4639e3b82.png">
</table>
<table>     
       <tr><td colspan="4"> <h4> #28 </h4>
    <tr><th> <a name="c28" id="c28"></a> commit id <td>a399b29dfbaaaf91162b2dc5a5875dd51bbfa2a1
        <th>kernel version      <td>3.10.21   
    <tr><th>module      <td>Process Management           <th>date                <td>2013/11/22
    <tr> <th>pattern             <td colspan="3">use after free   
    <tr> <th> description <td colspan="3">When IPC_RMID races with other shm operations there's potential for
use-after-free of the shm object's associated file (shm_file).
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8828820/a5c221ca-30c6-11e5-974d-0691c3ca6dd8.png">
</table>
<table>      
       <tr><td colspan="4"> <h4> #29 </h4>
    <tr><th> <a name="c29" id="c29"></a> commit id <td>c6c15e1ed303ffc47e696ea1c9a9df1761c1f603
        <th>kernel version      <td>3.10.62   
    <tr><th>module      <td>File System           <th>date                <td>2014/11/19
    <tr> <th>pattern             <td colspan="3">access without synchronization   
    <tr> <th> description <td colspan="3">The currect code for nfsd41_cb_get_slot() and nfsd4_cb_done() has no
locking in order to guarantee atomicity, and so allows for races of
the form.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8828832/b14ef978-30c6-11e5-8763-dba01d081101.png">
</table>
<table>      
       <tr><td colspan="4"> <h4> #30 </h4>
    <tr><th> <a name="c30" id="c30"></a> commit id <td>30a6b8031fe14031ab27c1fa3483cb9780e7f63c
        <th>kernel version      <td>3.17.3   
    <tr><th>module      <td>Others          <th>date                <td>2014/10/26
    <tr> <th>pattern             <td colspan="3">access with improper synchronization   
    <tr> <th> description <td colspan="3">free_pi_state and exit_pi_state_list both clean up futex_pi_state's.
exit_pi_state_list takes the hb lock first, and most callers of
free_pi_state do too. requeue_pi doesn't, which means free_pi_state
can free the pi_state out from under exit_pi_state_list.
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8828843/bc072dcc-30c6-11e5-80f3-7c14f5367e8c.png">
</table>
