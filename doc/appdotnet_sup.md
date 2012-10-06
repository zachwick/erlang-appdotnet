

#Module appdotnet_sup#
* [Description](#description)
* [Function Index](#index)
* [Function Details](#functions)


@todo Add description to appdotnet_sup.

__Behaviours:__ [`supervisor`](supervisor.md).

__Authors:__ erikh.<a name="index"></a>

##Function Index##


<table width="100%" border="1" cellspacing="0" cellpadding="2" summary="function index"><tr><td valign="top"><a href="#init-1">init/1</a></td><td><a href="http://www.erlang.org/doc/man/supervisor.html#Module:init-1">supervisor:init/1</a></td></tr><tr><td valign="top"><a href="#start_link-0">start_link/0</a></td><td></td></tr></table>


<a name="functions"></a>

##Function Details##

<a name="init-1"></a>

###init/1##


<pre>init(Args::term()) -&gt; Result</pre>
<ul class="definitions"><li><pre>Result = {ok, {SupervisionPolicy, [ChildSpec]}} | ignore</pre></li><li><pre>SupervisionPolicy = {RestartStrategy, MaxR::non_neg_integer(), MaxT::pos_integer()}</pre></li><li><pre>RestartStrategy = one_for_all | one_for_one | rest_for_one | simple_one_for_one</pre></li><li><pre>ChildSpec = {Id::term(), StartFunc, RestartPolicy, Type::worker | supervisor, Modules}</pre></li><li><pre>StartFunc = {M::module(), F::atom(), A::[term()] | undefined}</pre></li><li><pre>RestartPolicy = permanent | transient | temporary</pre></li><li><pre>Modules = [module()] | dynamic</pre></li></ul>

[supervisor:init/1](http://www.erlang.org/doc/man/supervisor.html#Module:init-1)<a name="start_link-0"></a>

###start_link/0##


<pre>start_link() -&gt; Result</pre>
<ul class="definitions"><li><pre>Result = {ok, pid()} | ignore | {error, StartlinkErr}</pre></li><li><pre>StartlinkErr = {already_started, pid()} | shutdown | term()</pre></li></ul>
