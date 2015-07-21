# KDR
List of Linux kernel data races found in recent 5 years
<br>
<h2>References:</h2>
<table>
<tr><td>
[1]<a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/"> Kernel.org git repositories </a>
<tr><td>
[2]<a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/"> Kernel.org git repositories </a>

</table>

<table>
    <tr> <th> list                      <th> source          <th> module         <th> version       <th> id     <th> status   
    <tr background="red";> <td> [<a href="#c1">1</a>]     <td> ChangeLog      <td> IO         <td> 3.10.8     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=d50235b7bc3ee0a0427984d763ea7534149531b4">d50235b7bc3ee0a0427984d763ea7534149531b4</a>    <td> Yes
    <tr> <td> [<a href="#c2">2</a>]     <td> ChangeLog      <td> Driver         <td> 3.0.38     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=8265981bb439f3ecc5356fb877a6c2a6636ac88a">8265981bb439f3ecc5356fb877a6c2a6636ac88a</a>    <td> Yes
    <tr> <td> [<a href="#c3">3</a>]     <td> ChangeLog      <td> Driver         <td> 3.0.59     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=ce73ec6db47af84d1466402781ae0872a9e7873c">ce73ec6db47af84d1466402781ae0872a9e7873c</a>    <td> Yes
    <tr> <td> [<a href="#c4">4</a>]     <td> ChangeLog      <td> KVM         <td> 3.10.60     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=2febc839133280d5a5e8e1179c94ea674489dae2">2febc839133280d5a5e8e1179c94ea674489dae2</a>    <td> Yes
    <tr> <td> [<a href="#c5">5</a>]     <td> ChangeLog      <td> KVM         <td> 3.3.6     
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=6dbf79e7164e9a86c1e466062c48498142ae6128">6dbf79e7164e9a86c1e466062c48498142ae6128</a>    <td> Yes
    <tr> <td> [<a href="#c6">6</a>]     <td> ChangeLog      <td> Block         <td> 3.10.23    
         <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=eb1c160b22655fd4ec44be732d6594fd1b1e44f4">eb1c160b22655fd4ec44be732d6594fd1b1e44f4</a>    <td> Yes
    <tr> <td> [<a href="#c7">7</a>]  	<td> ChangeLog 	<td> Driver             	<td> 3.1     	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=9c921c22a7f33397a6774d7fa076db9b6a0fd669">9c921c22a7f33397a6774d7fa076db9b6a0fd669 	<td> Yes 	
 <tr> <td> [<a href="#8">8</a>]  	<td> ChangeLog 	<td> Driver             	<td> 3.1     	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=7456caae37396fc1bc6f8e9461d07664b8c2f280">7456caae37396fc1bc6f8e9461d07664b8c2f280 	<td> Yes 	
<tr> <td> [<a href="#9">9</a>]   	<td> ChangeLog <td> Driver            <td> 3.0.11  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=5dc2470c602da8851907ec18942cd876c3b4ecc1">5dc2470c602da8851907ec18942cd876c3b4ecc1 	<td> Yes 	
<tr> <td> [<a href="#10">10</a>]  	<td> ChangeLog 	<td>Driver             	<td> 3.0.29  <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=a65a6f14dc24a90bde3f5d0073ba2364476200bf">a65a6f14dc24a90bde3f5d0073ba2364476200bf 	<td> Yes 
<tr> <td> [<a href="#11">11</a>]  	<td>ChangeLog <td> Driver             <td> 3.0.41  <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=44e4360fa3384850d65dd36fb4e6e5f2f112709b">44e4360fa3384850d65dd36fb4e6e5f2f112709b 	<td> Yes 	
<tr> <td> [<a href="#12">12</a>]  	<td> ChangeLog 	<td> Driver             	<td> 3.11.2  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=1eeeef153c02f5856ec109fa532eb5f31c39f85c">1eeeef153c02f5856ec109fa532eb5f31c39f85c 	<td>Yes 	
<tr> <td> [<a href="#13">13</a>]  	<td> ChangeLog <td> Driver             	<td> 3.10.34 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=ef0899410ff630b2e75306da49996dbbfa318165">ef0899410ff630b2e75306da49996dbbfa318165 	<td>Yes 
<tr> <td> [<a href="#14">14</a>]  	<td> ChangeLog 	<td>Driver             	<td> 3.10.23 <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=b869ccfab1e324507fa3596e3e1308444fb68227">b869ccfab1e324507fa3596e3e1308444fb68227 	<td>Yes 
<tr> <td> [<a href="#15">15</a>]  <td> ChangeLog <td> Driver             <td> 3.10.42 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=21f8aaee0c62708654988ce092838aa7df4d25d8">21f8aaee0c62708654988ce092838aa7df4d25d8 	<td> Yes 	
<tr> <td> [<a href="#16">16</a>]  	<td> ChangeLog 	<td> Driver             <td> 3.10.46 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=d9e93c08d8d985e5ef89436ebc9f4aad7e31559f">d9e93c08d8d985e5ef89436ebc9f4aad7e31559f 	<td> Yes 
<tr> <td> [<a href="#17">17</a>]  	<td> ChangeLog <td>File System        <td> 3.10.39 <td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=ec4cb1aa2b7bae18dd8164f2e9c7c51abcf61280">ec4cb1aa2b7bae18dd8164f2e9c7c51abcf61280 	<td> Yes 	
<tr> <td> [<a href="#18">18</a>]  	<td> ChangeLog 	<td> File System        <td> 3.2.45  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=794446c6946513c684d448205fbd76fa35f38b72">794446c6946513c684d448205fbd76fa35f38b72 	<td> Yes 
<tr> <td> [<a href="#19">19</a>]  	<td> ChangeLog <td> File System        	<td> 3.10.66 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=06bed7d18c2c07b3e3eeadf4bd357f6e806618cc">06bed7d18c2c07b3e3eeadf4bd357f6e806618cc 	<td> Yes 
<tr> <td> [<a href="#20">20</a>]  	<td> ChangeLog 	<td> File System        <td> 3.0.88  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=1c327d962fc420aea046c16215a552710bde8231">1c327d962fc420aea046c16215a552710bde8231 	<td> Yes 	
<tr> <td> [<a href="#21">21</a>]  	<td> ChangeLog 	<td> Process Management 	<td> 3.0.68  	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=71b5707e119653039e6e95213f00479668c79b75">71b5707e119653039e6e95213f00479668c79b75 	<td> Yes 
<tr> <td> [<a href="#22">22</a>]  	<td> ChangeLog 	<td> Process Management <td> 3.12.14 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=532de3fc72adc2a6525c4d53c07bf81e1732083d">532de3fc72adc2a6525c4d53c07bf81e1732083d 	<td> Yes 
<tr> <td> [<a href="#23">23</a>]  	<td> ChangeLog 	<td> Process Management 	<td> 3.12.37 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=c291ee622165cb2c8d4e7af63fffd499354a23be">c291ee622165cb2c8d4e7af63fffd499354a23be 	<td> Yes 
<tr> <td> [<a href="#24">24</a>]  	<td> ChangeLog 	<td>Process Management <td> 3.14.41 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=b72c186999e689cb0b055ab1c7b3cd8fffbeb5ed">b72c186999e689cb0b055ab1c7b3cd8fffbeb5ed 	<td> Yes 
<tr> <td> [<a href="#25">25</a>]  <td> ChangeLog 	<td> Memory Management  	<td> 3.12.36 	<td> <a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=91b57191cfd152c02ded0745250167d0263084f8">91b57191cfd152c02ded0745250167d0263084f8 	<td> Yes 	
         
</table>

<table>
     <tr><td colspan="4"> <h4> #2 </h4>
    <tr><th> <a name="c2" id="c2"></a> Commit id <td>d50235b7bc3ee0a0427984d763ea7534149531b4
        <th>Version      <td>3.10.8    
    <tr><th>Module      <td>IO           <th>Date                <td>2013/7/3
    <tr> <th>Pattern             <td colspan="3">use before initialization   
    <tr> <th>Description <td colspan="3">
    <tr> <th>Reproduce   <td colspan="3">
    <tr><th>Interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/4531815/8325292/c77a173e-1a8a-11e5-9ddd-7f7b8a3ac0a5.png">
    
    <tr><td colspan="4"> <h4> #2 </h4>
    <tr><th> <a name="c2" id="c2"></a> commit id <td>8265981bb439f3ecc5356fb877a6c2a6636ac88a
        <th>kernel version      <td>3.0.38    
    <tr><th>module      <td>IO           <th>date                <td>2012/7/13
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8777996/e5301c6c-2f2d-11e5-9c20-b5067b0ac989.png">
    
    <tr><td colspan="4"> <h4> #3 </h4>
    <tr><th> <a name="c3" id="c3"></a> commit id <td>ce73ec6db47af84d1466402781ae0872a9e7873c
        <th>kernel version      <td>3.0.38    
    <tr><th>module      <td>IO           <th>date                <td>2013/1/3
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8778028/14832356-2f2e-11e5-8542-ed5b210cd26e.png">
    
     <tr><td colspan="4"> <h4> #4 </h4>
    <tr><th> <a name="c4" id="c4"></a> commit id <td>2febc839133280d5a5e8e1179c94ea674489dae2
        <th>kernel version      <td>3.10.60    
    <tr><th>module      <td>IO           <th>date                <td>2014/10/24
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8778034/247a667a-2f2e-11e5-9ef6-a831beb2591b.png">
    
     <tr><td colspan="4"> <h4> #5 </h4>
    <tr><th> <a name="c5" id="c5"></a> commit id <td>6dbf79e7164e9a86c1e466062c48498142ae6128
        <th>kernel version      <td>3.3.6    
    <tr><th>module      <td>IO           <th>date                <td>2012/3/8
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8778041/2e47b568-2f2e-11e5-8cc8-83f16878dab1.png">
    
    
     <tr><td colspan="4"> <h4> #6 </h4>
    <tr><th> <a name="c6" id="c6"></a> commit id <td>eb1c160b22655fd4ec44be732d6594fd1b1e44f4
        <th>kernel version      <td>3.10.23    
    <tr><th>module      <td>IO           <th>date                <td>2013/11/8
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795136/c391b9a0-2fbc-11e5-9960-ba8287a19a15.png">
    
     <tr><td colspan="4"> <h4> #7 </h4>
    <tr><th> <a name="c7" id="c7"></a> commit id <td>9c921c22a7f33397a6774d7fa076db9b6a0fd669
        <th>kernel version      <td>3.1   
    <tr><th>module      <td>IO           <th>date                <td>2011/7/14
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795140/d09599a0-2fbc-11e5-940c-9e417a413bd0.png">
    
     <tr><td colspan="4"> <h4> #8 </h4>
    <tr><th> <a name="c8" id="c8"></a> commit id <td>7456caae37396fc1bc6f8e9461d07664b8c2f280
        <th>kernel version      <td>3.1   
    <tr><th>module      <td>IO           <th>date                <td>2011/7/20
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/12931943/8795143/d6550ee8-2fbc-11e5-98b0-2ee1b2db0db0.png">
    
    
</table>
