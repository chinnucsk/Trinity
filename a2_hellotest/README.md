Erlang Common Test: Minimal Test
================================
*b_hellotest*

This sample shows a minimal failing test.

The test simply crashes on itself. It has no subject file that it runs etc.

-----------------------------------------------------------------------

Note: this doc is in markdown, with HTML mixed in to show what you should see. Either you really do the samples steps yourself as proposed. Then you won't need the HTML. Otherwise, this doc is probably best viewed online at https://github.com/Eonblast/erlang-arcana/tree/master/b_hellotest

-----------------------------------------------------------------------


A Minimal, Failing Test
-----------------------

The test suite is in file `test/hello_SUITE.erl`, the source is basically:
      
      all() -> [my_test_case].
    
      my_test_case(_Config) -> "Foo" = "Bar".



Running the Test
----------------

Run the test like this:

      ./test.sh

This is what you should see:
    
    Paulchen:~/erlang-arcana-org/a2_hellotest me$ ./test.sh 
    Erlang R14B01 (erts-5.8.2) [source] [rq:1] [async-threads:0] [hipe] [kernel-poll:false]
    
    
    
    
    Common Test v1.5.2 starting (cwd is /Users/me/erlang-arcana-org/a2_hellotest)
    
    Eshell V5.8.2  (abort with ^G)
    (ct@Paulchen)1> 
    Common Test: Running make in test directories...
    Recompile: hello_SUITE
    ./hello_SUITE.erl:35: Warning: no clause will ever match
    
    CWD set to: "/Users/me/erlang-arcana-org/a2_hellotest/ct_run.ct@Paulchen.2011-12-12_22.11.18"
    
    TEST INFO: 1 test(s), 2 case(s) in 1 suite(s)
    
    Testing erlang-arcana-org.a2_hellotest: Starting test, 2 test cases
    
    - - - - - - - - - - - - - - - - - - - - - - - - - -
    hello_SUITE:my_test_case_2 failed on line 35
    Reason: {badmatch,"Bar"}
    - - - - - - - - - - - - - - - - - - - - - - - - - -
    
    Testing erlang-arcana-org.a2_hellotest: *** FAILED *** test case 2 of 2
    Testing erlang-arcana-org.a2_hellotest: TEST COMPLETE, 1 ok, 1 failed of 2 test cases
    
    Updating /Users/me/erlang-arcana-org/a2_hellotest/index.html... done
    Updating /Users/me/erlang-arcana-org/a2_hellotest/all_runs.html... done

Test Results
------------

To the see the test results, open:

      ./index.html

This is what you should see:

<div class=screen style="border:2px solid black; margin: 10px;">
<CENTER>
<H1>Test Results</H1>
</CENTER>
<BR>
<!-- ---- CONTENT ---- -->
<CENTER>

<A HREF="all_runs.html">All test runs in "a2_hellotest"</A>
<br><br>
<TABLE border="3" cellpadding="5" BGCOLOR="#E4F0FE">
<th>Test Name</th>
<th>Label</th>
<th>Test Run Started</th>
<th><font color="#E4F0FE">_</font>Ok<font color="#E4F0FE">_</font></th>
<th>Failed</th>
<th>Skipped<br>(User/Auto)</th>

<th>Missing<br>Suites</th>
<th>Node</th>
<th>CT Log</th>
<th>Old Runs</th>

<TR valign=top>
<TD><FONT SIZE=-1><A HREF="ct_run.ct@machine.2011-12-12_22.11.18/erlang-arcana-org.a2_hellotest.logs/run.2011-12-12_22.11.21/suite.log.html">erlang-arcana-org.a2_hellotest</A></FONT></TD>
<TD ALIGN=center><FONT SIZE=-1><B>-</FONT></B></TD>
<TD><FONT SIZE=-1>Mon Dec 12 2011 22:11:18</FONT></TD>

<TD ALIGN=right>1</TD>
<TD ALIGN=right><FONT color="red">1</FONT></TD>
<TD ALIGN=right>0 (0/0)</TD>
<TD ALIGN=right>0</TD>
<TD ALIGN=right><FONT SIZE=-1>ct@machine</FONT></TD>
<TD><FONT SIZE=-1><A HREF="ct_run.ct@machine.2011-12-12_22.11.18/ctlog.html">CT Log</A></FONT></TD>
<TD><FONT SIZE=-1>none</FONT></TD>
</TR>
<TR valign=top>
<TD><B>Total</B></TD><TD>&nbsp;</TD>

<TD>&nbsp;</TD>
<TD ALIGN=right><B>1<B></TD>
<TD ALIGN=right><B>1<B></TD>
<TD ALIGN=right>0 (0/0)</TD>
<TD ALIGN=right><B>0<B></TD>
<TD>&nbsp;</TD>
<TD>&nbsp;</TD>
</TR>
</TABLE>
</CENTER>
<P><CENTER>
<BR><BR>
<HR>

<P><FONT SIZE=-1>
Copyright &copy; 2011 <A HREF="http://erlang.ericsson.se">Open Telecom Platform</A><BR>
Updated: <!date>Mon Dec 12 2011 22:11:22<!/date><BR>
</FONT>
</CENTER>

</div>

Digging Deeper
--------------

Clicking on the Test Name, you'll find the details in the next screen:

<div class=screen style="border:2px solid black; margin: 10px;">
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<!-- autogenerated by 'test_server_ctrl'. -->
<html>
<head><title>Test "erlang-arcana-org.a2_hellotest" results</title>
<meta http-equiv="cache-control" content="no-cache">
</head>
<body background="/opt/local/lib/erlang/lib/common_test-1.5.2/priv/tile1.jpg" bgcolor="white" text="black" link="blue" vlink="purple" alink="red">
<H2>Results from test "erlang-arcana-org.a2_hellotest"</H2>
Test started at 2011-12-12 22:11:22<p>Host:<br>
Run by hd on Paulchen<br>Used Erlang 5.8.2 in <tt>/opt/local/lib/erlang</tt>.

<p><a href="suite.log">Full textual log</a>
<br><a href="cover.html">Coverage log</a>
<p>Suite contains 2 test cases.
<p>
<table bgcolor="white" border="3" cellpadding="5"><tr><th>Num</th><th>Module</th><th>Case</th><th>Log</th><th>Time</th><th>Result</th><th>Comment</th></tr>
<tr valign=top><td><font color="black">1</font></td><td><font color="black">hello_SUITE</font></td><td><a href="hello_suite.my_test_case_1.html">my_test_case_1</a></td><td><a href="hello_suite.my_test_case_1.html#top"><</a> <a href="hello_suite.my_test_case_1.html#end">></a></td><td><font color="black">0.000s</font></td><td><font color="green">Ok</font></td></tr>

<tr valign=top><td><font color="black">2</font></td><td><font color="black">hello_SUITE</font></td><td><a href="hello_suite.my_test_case_2.html">my_test_case_2</a></td><td><a href="hello_suite.my_test_case_2.html#top"><</a> <a href="hello_suite.my_test_case_2.html#end">></a></td><td><font color="black">0.000s</font></td><td><font color="red">FAILED</font></td><td><font color="red">{hello_SUITE,my_test_case_2,<a href="hello_suite.src.html#30">35</a>}</font><br><font color="brown">{badmatch,"Bar"}</font></td></tr>
<tr><td></td><td><b>TOTAL</b></td><td></td><td></td><td>0.614s</td><td><b>FAILED</b></td><td>1 Ok, 1 Failed of 2</td></tr>

</table>
</body>
</html>
 </div>

## Cleaning

If you run the tests a couple of times, you'll get an archive of test results, index.html, all_runs.html and a couple of subdirectories.

To start over, clean the directory using 

      ./clean.sh
      

## Next

The next tutorial step is in folder `../b_hellotest2`.
Online at https://github.com/Eonblast/erlang-arcana/tree/master/b_hellotest2

While this test was a minimal suite, the next one is a full skeleton with stubs for all elements that a full fledged test suite would see.


-----------------------------------------------------------------------

If you want to add to this very text, please use github preview:
http://github.github.com/github-flavored-markdown/preview.html

-----------------------------------------------------------------------
Erlang Arcana Tutorial
&copy; 2011 Eonblast Corporation http://www.eonblast.com. MIT Open Source License.
