# KDR
List of Linux kernel data races found in recent 5 years
<br>
<h2>References:</h2>
<table>
<tr><td>
[1]<a href="https://bugzilla.kernel.org">Kernel Bug Tracker</a>
<tr><td>
[2]<a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/"> Kernel.org git repositories </a>

</table>

<table>
    <tr> <th> list                      <th> source          <th> module         <th> version       <th> id     <th> date <th>status

<tr><td>[<a href='#c1'>1</a>]<td>Bugzilla<td>ACPI<td>2.6.39<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=35642'>35642</a><td>Resolved
<tr><td>[<a href='#c2'>2</a>]<td>Bugzilla<td>ACPI<td>3.12<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=70891'>70891</a><td>Resolved
<tr><td>[<a href='#c3'>3</a>]<td>Bugzilla<td>Drivers<td>2.6.38.x<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=34992'>34992</a><td>Resolved
<tr><td>[<a href='#c4'>4</a>]<td>Bugzilla<td>Drivers<td>3.2.10<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=42916'>42916</a><td>Resolved
<tr><td>[<a href='#c5'>5</a>]<td>Bugzilla<td>Drivers<td>3.3.1-3.3.4<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=43187'>43187</a><td>Resolved
<tr><td>[<a href='#c6'>6</a>]<td>Bugzilla<td>Drivers<td>vanilla 3.4-rc1<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=43044'>43044</a><td>Opened
<tr><td>[<a href='#c7'>7</a>]<td>Bugzilla<td>Drivers<td>2.6.25<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=45691'>45691</a><td>Opened
<tr><td>[<a href='#c8'>8</a>]<td>Bugzilla<td>Drivers<td>2.6.32.7<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=15294'>15294</a><td>Resolved
<tr><td>[<a href='#c9'>9</a>]<td>Bugzilla<td>Drivers<td>2.6.34-rc4<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=15550'>15550</a><td>Resolved
<tr><td>[<a href='#c10'>10</a>]<td>Bugzilla<td>Drivers<td>3.6.6<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=50461'>50461</a><td>Resolved
<tr><td>[<a href='#c11'>11</a>]<td>Bugzilla<td>Drivers<td>3.7<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=52471'>52471</a><td>Resolved
<tr><td>[<a href='#c12'>12</a>]<td>Bugzilla<td>Drivers<td>3.9<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=57321'>57321</a><td>Resolved
<tr><td>[<a href='#c13'>13</a>]<td>Bugzilla<td>Drivers<td>3.8.13<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=57381'>57381</a><td>Resolved
<tr><td>[<a href='#c14'>14</a>]<td>Bugzilla<td>Drivers<td>3.2.45<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=58511'>58511</a><td>Resolved
<tr><td>[<a href='#c15'>15</a>]<td>Bugzilla<td>Drivers<td>3.7+<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=58971'>58971</a><td>Resolved
<tr><td>[<a href='#c16'>16</a>]<td>Bugzilla<td>Drivers<td>3.4.46<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=60719'>60719</a><td>Opened
<tr><td>[<a href='#c17'>17</a>]<td>Bugzilla<td>Drivers<td>3.11-rc7<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=60811'>60811</a><td>Resolved
<tr><td>[<a href='#c18'>18</a>]<td>Bugzilla<td>Drivers<td>3.4.46<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=60719'>60719</a><td>Opened
<tr><td>[<a href='#c19'>19</a>]<td>Bugzilla<td>Drivers<td>3.12-rc7<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=64361'>64361</a><td>Resolved
<tr><td>[<a href='#c20'>20</a>]<td>Bugzilla<td>Drivers<td>3.13<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=69611'>69611</a><td>Resolved
<tr><td>[<a href='#c21'>21</a>]<td>Bugzilla<td>Drivers<td>3.13.5<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=71551'>71551</a><td>Resolved
<tr><td>[<a href='#c22'>22</a>]<td>Bugzilla<td>Drivers<td>3.14.2<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=75561'>75561</a><td>Opened
<tr><td>[<a href='#c23'>23</a>]<td>Bugzilla<td>Drivers<td>3.16.1<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=83611'>83611</a><td>Opened
<tr><td>[<a href='#c24'>24</a>]<td>Bugzilla<td>File System<td>2.6.35-rc3<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=16312'>16312</a><td>Resolved
<tr><td>[<a href='#c25'>25</a>]<td>Bugzilla<td>File System<td>2.6.37<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=29752'>29752</a><td>Resolved
<tr><td>[<a href='#c26'>26</a>]<td>Bugzilla<td>File System<td>2.6.39-rc2<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=36002'>36002</a><td>Resolved
<tr><td>[<a href='#c27'>27</a>]<td>Bugzilla<td>File System<td>2.6.31.6<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=14739'>14739</a><td>Resolved
<tr><td>[<a href='#c28'>28</a>]<td>Bugzilla<td>File System<td>Linux-2.6.24.7<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=15572'>15572</a><td>Resolved
<tr><td>[<a href='#c29'>29</a>]<td>Bugzilla<td>File System<td>3.7-rc7<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=50991'>50991</a><td>Resolved
<tr><td>[<a href='#c30'>30</a>]<td>Bugzilla<td>File System<td>3.6.0, 3.5.x<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=48421'>48421</a><td>Resolved
<tr><td>[<a href='#c31'>31</a>]<td>Bugzilla<td>File System<td>3.2.0-29-generic<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=51391'>51391</a><td>Resolved
<tr><td>[<a href='#c32'>32</a>]<td>Bugzilla<td>File System<td>3.9-rc4<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=55651'>55651</a><td>Resolved
<tr><td>[<a href='#c33'>33</a>]<td>Bugzilla<td>File System<td>3.0<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=65241'>65241</a><td>Opened
<tr><td>[<a href='#c34'>34</a>]<td>Bugzilla<td>File System<td>3.11-rc6<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=60786'>60786</a><td>Opened
<tr><td>[<a href='#c35'>35</a>]<td>Bugzilla<td>File System<td>3.2.0<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=72041'>72041</a><td>Opened
<tr><td>[<a href='#c36'>36</a>]<td>Bugzilla<td>File System<td>2.4.37/2.6.32/3.2-3.18<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=91881'>91881</a><td>Opened
<tr><td>[<a href='#c37'>37</a>]<td>Bugzilla<td>File System<td>all<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=93441'>93441</a><td>Opened
<tr><td>[<a href='#c38'>38</a>]<td>Bugzilla<td>File System<td>3.0<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=62221'>62221</a><td>Opened
<tr><td>[<a href='#c39'>39</a>]<td>Bugzilla<td>IO<td>2.6.38-rc5<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=29442'>29442</a><td>Resolved
<tr><td>[<a href='#c40'>40</a>]<td>Bugzilla<td>IO<td>2.6.38<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=31802'>31802</a><td>Resolved
<tr><td>[<a href='#c41'>41</a>]<td>Bugzilla<td>IO<td>2.6.20.1<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=8223'>8223</a><td>Resolved
<tr><td>[<a href='#c42'>42</a>]<td>Bugzilla<td>IO<td>/<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=32552'>32552</a><td>Resolved
<tr><td>[<a href='#c43'>43</a>]<td>Bugzilla<td>IO<td>3.3<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=12309'>12309</a><td>Resolved
<tr><td>[<a href='#c44'>44</a>]<td>Bugzilla<td>Memory Management<td>2.6.28<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=15723'>15723</a><td>Resolved
<tr><td>[<a href='#c45'>45</a>]<td>Bugzilla<td>Memory Management<td>3.8.12<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=58011'>58011</a><td>Resolved
<tr><td>[<a href='#c46'>46</a>]<td>Bugzilla<td>Memory Management<td>3.18-rc4 and all earlier versions<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=88051'>88051</a><td>Resolved
<tr><td>[<a href='#c47'>47</a>]<td>Bugzilla<td>Memory Management<td>3.16.0-rc5<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=80881'>80881</a><td>Opened
<tr><td>[<a href='#c48'>48</a>]<td>Bugzilla<td>Process Management<td>2.6.36.3<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=27142'>27142</a><td>Resolved
<tr><td>[<a href='#c49'>49</a>]<td>Bugzilla<td>Process Management<td>3.4,3.10<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=61451'>61451</a><td>Opened
<tr><td>[<a href='#c50'>50</a>]<td>Bugzilla<td>Networking<td>2.6.31<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=15606'>15606</a><td>Resolved
<tr><td>[<a href='#c51'>51</a>]<td>Bugzilla<td>Networking<td>3.4.0<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=59951'>59951</a><td>Opened
<tr><td>[<a href='#c52'>52</a>]<td>Bugzilla<td>Networking<td>3.5.0+(earlier versions untested)<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=52991'>52991</a><td>Opened
<tr><td>[<a href='#c53'>53</a>]<td>Bugzilla<td>Others<td>3.0.1, 3.0.3<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=42382'>42382</a><td>Resolved
<tr><td>[<a href='#c54'>54</a>]<td>Bugzilla<td>Others<td>3.0.10, 3.0.11<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=61371'>61371</a><td>Opened
