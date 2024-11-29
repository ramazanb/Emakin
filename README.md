# Emakin BPM Helper Libraries

## AltiKareUtils | Utility Libraries & Processes
<p>
  Provides utility processes and helper libraries for both client and server side scripting.
</p>

### Installation
<p>
  Process graph is in AltiKareUtils.txt file. Simply create a process for central configuration purposses, and paste file contents. 
  You now have a central configuration where you can define a tree like structured data to be used in other processes. 
</p>
<p>
  You can also use the process as your projects configuration interface To achieve this;
  - Copy process to your project folder.</li>
  - Change context name in module script "Config" to match your project name. (Use UPPER_CASE syntax for better standardisation)</li>
  </ol>
  Now you have an interface to configure your process.
</p>

### Multi Tenant Configuration
<p>Configuration system is inherited like multi-tenant config -> domain config -> user config. Multi tenant DB is optional and can be used by registering utilities process graph on server command line. You can register a multi tenant DB store as below.</p>

```
AltiKare.Workflow.Agent.exe registerstore "mycompany.com" "PS_GLB" "AltiKareUtils.txt"
```

> [!NOTE]
> PS_ prefix is required. mycompany.com is application name in Emakin system.
> You will need to set GLOBAL_STORE_NAME variable on top of utilities module script as PS_GLB to make it useable. (Currently no autodetect method is available).

### Referencing / Usage
<p>
  Utils project have a utility module script named "AltiKareUtils". Copy it to your processes to use.
  Currently module script sharing does not work on Oracle based Emakin, nor it refresh referenced processes with latest version on other DB based ones. 
  So for now, just copy module script contents to your processes and manually refresh it as needed.
  This may change in future versions of Emakin, so stay tuned.
</p>
<p>Methods are exposed over AltiKareUtils namespace followed by utility class name. (e.g.: AltiKareUtils.Xml.parse(...) method).</p>

> [!NOTE]
> Util library uses a CONTEXT named constant to isolate between processes. Either define this in Config named script module or variable in pool to use methods.

### Libraries
<p>
  Below libraries are provided with project:
</p>

- <a href="https://github.com/ramazanb/Emakin/blob/master/AltiKareUtils.Text.md">AltiKareUtils.Text</a>
- <a href="https://github.com/ramazanb/Emakin/blob/master/AltiKareUtils.Xml.md">AltiKareUtils.Xml</a>
- <a href="https://github.com/ramazanb/Emakin/blob/master/AltiKareUtils.Config.md">AltiKareUtils.Config</a>
- <a href="https://github.com/ramazanb/Emakin/blob/master/AltiKareUtils.Sequence.md">AltiKareUtils.Sequence</a>
