# KDR
List of Linux kernel data races found in recent 5 years
<br>
<h2>References:</h2>
<table>
<tr><td>
[1]<a href="https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/"> Kernel.org git repositories </a>
<tr><td>
[2]<a href="https://www.kernel.org">The Linux Kernel Archives</a>

</table>

<table>
    <tr> <th> list                      <th> source          <th> module         <th> version       <th> id     <th> date <th>status

<tr><td>[<a href='#c1'>1</a>]<td>Bugzilla<td>ACPI<td>35642<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.39'>2.6.39</a><td>2011/5/23<td>Resolved
<tr><td>[<a href='#c2'>2</a>]<td>Bugzilla<td>ACPI<td>70891<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.12'>3.12</a><td>2014/2/20<td>Resolved
<tr><td>[<a href='#c3'>3</a>]<td>Bugzilla<td>Drivers<td>34992<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.38.x'>2.6.38.x</a><td>2011/5/12<td>Resolved
<tr><td>[<a href='#c4'>4</a>]<td>Bugzilla<td>Drivers<td>42916<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.2.10'>3.2.10</a><td>2012/3/13<td>Resolved
<tr><td>[<a href='#c5'>5</a>]<td>Bugzilla<td>Drivers<td>43187<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.3.1-3.3.4'>3.3.1-3.3.4</a><td>2012/5/1<td>Resolved
<tr><td>[<a href='#c6'>6</a>]<td>Bugzilla<td>Drivers<td>43044<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=vanilla 3.4-rc1'>vanilla 3.4-rc1</a><td>2012/4/4<td>Opened
<tr><td>[<a href='#c7'>7</a>]<td>Bugzilla<td>Drivers<td>45691<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.25'>2.6.25</a><td>2012/8/7<td>Opened
<tr><td>[<a href='#c8'>8</a>]<td>Bugzilla<td>Drivers<td>15294<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.32.7'>2.6.32.7</a><td>2010/2/14<td>Resolved
<tr><td>[<a href='#c9'>9</a>]<td>Bugzilla<td>Drivers<td>15550<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.34-rc4'>2.6.34-rc4</a><td>2010/3/16<td>Resolved
<tr><td>[<a href='#c10'>10</a>]<td>Bugzilla<td>Drivers<td>50461<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.6.6'>3.6.6</a><td>2012/11/13<td>Resolved
<tr><td>[<a href='#c11'>11</a>]<td>Bugzilla<td>Drivers<td>52471<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.7'>3.7</a><td>2013/1/8<td>Resolved
<tr><td>[<a href='#c12'>12</a>]<td>Bugzilla<td>Drivers<td>57321<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.9'>3.9</a><td>2013/4/30<td>Resolved
<tr><td>[<a href='#c13'>13</a>]<td>Bugzilla<td>Drivers<td>57381<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.8.13'>3.8.13</a><td>2013/05/01?<td>Resolved
<tr><td>[<a href='#c14'>14</a>]<td>Bugzilla<td>Drivers<td>58511<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.2.45'>3.2.45</a><td>2013/5/19<td>Resolved
<tr><td>[<a href='#c15'>15</a>]<td>Bugzilla<td>Drivers<td>58971<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.7+'>3.7+</a><td>2013/5/29<td>Resolved
<tr><td>[<a href='#c16'>16</a>]<td>Bugzilla<td>Drivers<td>60719<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.4.46'>3.4.46</a><td>2013/8/8<td>Opened
<tr><td>[<a href='#c17'>17</a>]<td>Bugzilla<td>Drivers<td>60811<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.11-rc7'>3.11-rc7</a><td>2013/8/29<td>Resolved
<tr><td>[<a href='#c18'>18</a>]<td>Bugzilla<td>Drivers<td>60719<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.4.46'>3.4.46</a><td>2013/8/8<td>Opened
<tr><td>[<a href='#c19'>19</a>]<td>Bugzilla<td>Drivers<td>64361<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.12-rc7'>3.12-rc7</a><td>2013/11/4<td>Resolved
<tr><td>[<a href='#c20'>20</a>]<td>Bugzilla<td>Drivers<td>69611<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.13'>3.13</a><td>2014/1/28<td>Resolved
<tr><td>[<a href='#c21'>21</a>]<td>Bugzilla<td>Drivers<td>71551<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.13.5'>3.13.5</a><td>2014/3/5<td>Resolved
<tr><td>[<a href='#c22'>22</a>]<td>Bugzilla<td>Drivers<td>75561<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.14.2'>3.14.2</a><td>2014/5/6<td>Opened
<tr><td>[<a href='#c23'>23</a>]<td>Bugzilla<td>Drivers<td>83611<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.16.1'>3.16.1</a><td>2014/8/31<td>Opened
<tr><td>[<a href='#c24'>24</a>]<td>Bugzilla<td>File System<td>16312<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.35-rc3'>2.6.35-rc3</a><td>2010/6/28<td>Resolved
<tr><td>[<a href='#c25'>25</a>]<td>Bugzilla<td>File System<td>29752<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.37'>2.6.37</a><td>2011/2/23<td>Resolved
<tr><td>[<a href='#c26'>26</a>]<td>Bugzilla<td>File System<td>36002<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.39-rc2'>2.6.39-rc2</a><td>2011/5/27<td>Resolved
<tr><td>[<a href='#c27'>27</a>]<td>Bugzilla<td>File System<td>14739<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.31.6'>2.6.31.6</a><td>2009/12/5<td>Resolved
<tr><td>[<a href='#c28'>28</a>]<td>Bugzilla<td>File System<td>15572<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=Linux-2.6.24.7'>Linux-2.6.24.7</a><td>2010/3/18<td>Resolved
<tr><td>[<a href='#c29'>29</a>]<td>Bugzilla<td>File System<td>50991<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.7-rc7'>3.7-rc7</a><td>2012/11/26<td>Resolved
<tr><td>[<a href='#c30'>30</a>]<td>Bugzilla<td>File System<td>48421<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.6.0, 3.5.x'>3.6.0, 3.5.x</a><td>2012-10-05?<td>Resolved
<tr><td>[<a href='#c31'>31</a>]<td>Bugzilla<td>File System<td>51391<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.2.0-29-generic'>3.2.0-29-generic</a><td>2012/12/7<td>Resolved
<tr><td>[<a href='#c32'>32</a>]<td>Bugzilla<td>File System<td>55651<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.9-rc4'>3.9-rc4</a><td>2013/3/23<td>Resolved
<tr><td>[<a href='#c33'>33</a>]<td>Bugzilla<td>File System<td>65241<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.0'>3.0</a><td>2013/11/20<td>Opened
<tr><td>[<a href='#c34'>34</a>]<td>Bugzilla<td>File System<td>60786<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.11-rc6'>3.11-rc6</a><td>2013/8/23<td>Opened
<tr><td>[<a href='#c35'>35</a>]<td>Bugzilla<td>File System<td>72041<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.2.0'>3.2.0</a><td>2014/3/14<td>Opened
<tr><td>[<a href='#c36'>36</a>]<td>Bugzilla<td>File System<td>91881<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.4.37/2.6.32/3.2-3.18'>2.4.37/2.6.32/3.2-3.18</a><td>2015/1/23<td>Opened
<tr><td>[<a href='#c37'>37</a>]<td>Bugzilla<td>File System<td>93441<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=all'>all</a><td>2015/2/18<td>Opened
<tr><td>[<a href='#c38'>38</a>]<td>Bugzilla<td>File System<td>62221<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.0'>3.0</a><td>2013/9/27<td>Opened
<tr><td>[<a href='#c39'>39</a>]<td>Bugzilla<td>IO<td>29442<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.38-rc5'>2.6.38-rc5</a><td>2011/2/19<td>Resolved
<tr><td>[<a href='#c40'>40</a>]<td>Bugzilla<td>IO<td>31802<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.38'>2.6.38</a><td>2011/3/24<td>Resolved
<tr><td>[<a href='#c41'>41</a>]<td>Bugzilla<td>IO<td>8223<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.20.1'>2.6.20.1</a><td>2007/3/16<td>Resolved
<tr><td>[<a href='#c42'>42</a>]<td>Bugzilla<td>IO<td>32552<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=/'>/</a><td>2011/4/3<td>Resolved
<tr><td>[<a href='#c43'>43</a>]<td>Bugzilla<td>IO<td>12309<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.3'>3.3</a><td>2011/4/3<td>Resolved
<tr><td>[<a href='#c44'>44</a>]<td>Bugzilla<td>Memory Management<td>15723<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.28'>2.6.28</a><td>2010/4/8<td>Resolved
<tr><td>[<a href='#c45'>45</a>]<td>Bugzilla<td>Memory Management<td>58011<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.8.12'>3.8.12</a><td>2013/5/11<td>Resolved
<tr><td>[<a href='#c46'>46</a>]<td>Bugzilla<td>Memory Management<td>88051<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.18-rc4 and all earlier versions'>3.18-rc4 and all earlier versions</a><td>2014/11/11<td>Resolved
<tr><td>[<a href='#c47'>47</a>]<td>Bugzilla<td>Memory Management<td>80881<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.16.0-rc5'>3.16.0-rc5</a><td>2014/7/22<td>Opened
<tr><td>[<a href='#c48'>48</a>]<td>Bugzilla<td>Process Management<td>27142<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.36.3'>2.6.36.3</a><td>2011/1/20<td>Resolved
<tr><td>[<a href='#c49'>49</a>]<td>Bugzilla<td>Process Management<td>61451<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.4,3.10'>3.4,3.10</a><td>2013/9/16<td>Opened
<tr><td>[<a href='#c50'>50</a>]<td>Bugzilla<td>Networking<td>15606<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=2.6.31'>2.6.31</a><td>2010/3/22<td>Resolved
<tr><td>[<a href='#c51'>51</a>]<td>Bugzilla<td>Networking<td>59951<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.4.0'>3.4.0</a><td>2013/6/20<td>Opened
<tr><td>[<a href='#c52'>52</a>]<td>Bugzilla<td>Networking<td>52991<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.5.0+(earlier versions untested)'>3.5.0+(earlier versions untested)</a><td>2013/1/24<td>Opened
<tr><td>[<a href='#c53'>53</a>]<td>Bugzilla<td>Others<td>42382<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.0.1, 3.0.3'>3.0.1, 3.0.3</a><td>2011/9/5<td>Resolved
<tr><td>[<a href='#c54'>54</a>]<td>Bugzilla<td>Others<td>61371<td><a href='https://bugzilla.kernel.org/show_bug.cgi?id=3.0.10, 3.0.11'>3.0.10, 3.0.11</a><td>2013/9/15<td>Opened
