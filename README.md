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
         <td> <a href="#c1">d50235b7bc3ee0a0427984d763ea7534149531b4</a>    <td> Yes
</table>

<table>
    <tr><th> <a name="c2" id="c2"></a> commit id <td>d50235b7bc3ee0a0427984d763ea7534149531b4
        <th>kernel version      <td>3.10.8    
    <tr><th>module      <td>IO           <th>date                <td>2013/7/3
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/4531815/8325292/c77a173e-1a8a-11e5-9ddd-7f7b8a3ac0a5.png">
    <tr><td colspan="4"> <hr width="100%" height="2px" color="#ff0000">
    <tr><th> <a name="c1" id="c1"></a> commit id <td>d50235b7bc3ee0a0427984d763ea7534149531b4
        <th>kernel version      <td>3.10.8    
    <tr><th>module      <td>IO           <th>date                <td>2013/7/3
    <tr> <th>pattern             <td colspan="3">use before initialization   
    <tr> <th> description <td colspan="3">
    <tr> <th> reproduce   <td colspan="3">
    <tr><th>interleaving 
    <td colspan="3"><image src="https://cloud.githubusercontent.com/assets/4531815/8325292/c77a173e-1a8a-11e5-9ddd-7f7b8a3ac0a5.png">
</table>
