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
    <tr> <th> list                      <th> source          <th> module         <th> version       <th> id      
    <tr background="red";> <td> [<a href="#c1">1</a>]     <td> ChangeLog      <td> IO         <td> 3.10.8     
         <td> <a href="#c1">d50235b7bc3ee0a0427984d763ea7534149531b4</a>   
</table>

<table>
    <tr><td> <a name="c1" id="c1"></a> commit id <td>d50235b7bc3ee0a0427984d763ea7534149531b4
        <td>kernel version      <td>3.10.8    
    <tr><td>kernel module<td>IO    
        <td>date                <td>2013/7/3
    <tr><td>pattern             <td>use before initialization    
    <tr><td>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/4531815/8325292/c77a173e-1a8a-11e5-9ddd-7f7b8a3ac0a5.png">
</table>
