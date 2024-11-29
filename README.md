<h1>Emakin BPM Helper Libraries</h1>

<h2>AltiKareUtils | Utility Libraries & Processes</h2>
<p>
  Provides utility processes and helper libraries for both client and server side scripting.
</p>

<h3>Intallation</h3>
<p>
  Process graph is in AltiKareUtils.txt file. Simply create a process for central configuration purposses, and paste file contents. 
  You now have a central configuration where you can define a tree like structured data to be used in other processes. 
</p>
<p>
  You can also use the process as your projects configuration interface To achieve this;
  <ol>
    <li>Copy process to your project folder.</li>
    <li>Change context name in module script "Config" to match your project name. (Use UPPER_CASE syntax for better standardisation)</li>
  </ol>
  Now you have an interface to configure your process.
</p>

<h3>Referencing / Usage</h3>
<p>
  Utils project have a utility module script named "AltiKareUtils". Copy it to your processes to use.
  Currently module script sharing does not work on Oracle based Emakin, nor it refresh referenced processes with latest version on other DB based ones. 
  So for now, just copy module script contents to your processes and manually refresh it as needed.
  This may change in future versions of Emakin, so stay tuned.
</p>
<p>Util library uses a CONTEXT named constant to isolate between processes. Either define this in another script module or pool to use methods.</p>
<p>Methods are exposed over AltiKareUtils namespace followed by utility class name. (e.g.: AltiKareUtils.Xml.parse(...) method).</p>

<h3>Libraries</h3>
<p>
  Below libraries are provided with project:
</p>
<ul>
  <li><a href="https://github.com/ramazanb/Emakin/blob/master/README.Text.md#text-utilities">AltiKareUtils.Text</a></li>
  <li><a href="https://github.com/ramazanb/Emakin/blob/master/README.Xml.md#xml-utilities">AltiKareUtils.Xml</a></li>
  <li><a href="https://github.com/ramazanb/Emakin/blob/master/README.Config.md#config-utilities">AltiKareUtils.Config</a></li>
  <li><a href="https://github.com/ramazanb/Emakin/blob/master/README.Sequence.md#sequence-utilities">AltiKareUtils.Sequence</a></li>
</ul>
