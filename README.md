---
layout: default
---


<p align="center">
    <img src="docs/img/NagiosLogo.png"
        alt="Master">
</p>

<p align="center">
  <a href="https://github.com/dolbyjoab/101-nagios/tree/master">
    <img src="https://img.shields.io/badge/Branch-master-green.svg?longCache=true"
        alt="Branch">
  </a>
  <a href="http://www.gnu.org/licenses/">
    <img src="https://img.shields.io/badge/License-GNU-blue.svg?longCache=true"
        alt="License">
  </a>
</p>

***

## <a name="Introduction">Introduction</a>

<p align="justify"> Nagios is a server monitoring infrastructure. In the olds days we used to have to run horribly cryptics commands like <b>sar, ps, du, df, and others,</b> then parse the output with awk and sed and then figure out how to do something with the data. These commands were never standardized so scripts running under Solaris may not work as expected under SunOS! Things gradually evolved and Nagios came on the scene almost 20 years ago. Nagios is now used to monitor sites with hundreds of thousands of services and you can configure tiered monitoring if you need maximum scalability. Nagios is incredibly flexible, but its greatest strength is also its weakness. Its power comes from the fact that it is based on scripting, allowing you to monitor literally anything. It's notification system is also based on scripts, so you can do whatever you like with the information, even restart services, clean old logs, or whatever. You can even download pre-written scripts to extend Nagios in all sorts of ways. Check the Nagios website for a repository.
</p>

***

## <a name="Contribuing">Contributing</a>

ℹ️ This project contains **examples** of test questions and answers that can be used during an interview or exam for positions such as **Nagios Administrator** or just to refresh your memory.<br>
⚠️ Questions marked with a '<b>*</b>' don't have answers yet - just make a pull request to add them!<br>
‼ The answers may be explicit examples, don't need to exhaust the whole topic.<br>
👮🏾‍♂️ If you find a question which doesn't make sense, or one of the answers doesn't seem right; please make a pull request! Feedback and advice is welcome.
<br>
If you would like to support this project, you have an interesting idea how to improve the operation of this tool or if you found some errors - do fork this add your fixes and add pull-request of your branch to the **dev branch**.

**Remember:**
- <a href="https://github.com/dolbyjoab/101-nagios/fork">Fork the repository</a>
- Base your code on the latest master branch to avoid manual merges
- Code review may ensue in order to help shape your proposal
- Explain the problem and your proposed solution
- Make your changes in **index.md**
- Send a pull-request to the **dev branch**

***

## <a name="Questions">General</a>
<details>
<summary><b>Explain Nagios or what is Nagios, explain it.</b></summary><br>
<p align="justify">Nagios is a monitoring tool that is used for continuous monitoring of system services, applications, and business processes. Even in case of any failure, Nagios tool can alert the technical staff about the problem. As a result, DevOps professionals or technical team members can begin the required remediation processes before the negative impact of any business processes, customers, and end-users. Here, in such cases, the team does not have to explain anyone that why an unseen infrastructure outage affects the bottom line of the organization.</p>

Let's mention a few things that can be achieved by Nagios:

<ul>
<li> Automatic problem fixing as and when they occur.</li>
<li> Infrastructure upgrades planning even before any failure due to an outdated system.</li>
<li> Technical team response coordination.</li>
<li> To ensure that SLA of your organization will be met.</li>
<li> To monitor the business process and the entire infrastructure.</li>
<li> To respond to issues even as and when they arise.</li>
</ul>
</details>


<details>
<summary><b>Explain the working of Nagios, how does it work?</b></summary><br>
<p align="justify">On a server, Nagios either runs as a service or daemon. Plugins that resides on the same server are being run by the Nagios; basically, they contact the hosts or servers of your network or on the internet. We can check the status by web interface; even notifications can also be received by email or SMS when something happens.</p>

Nagios service runs certain scripts after a fix time interval, so it acts as a scheduler. It can store the script result and run other scripts when it is changed.
</details>


<details>
<summary><b>Explain Nagios plugins.</b></summary><br>
<p align="justify">Plugins are basically scripts of Perl and Shell that can be run through the command line to check the service status of the host. Nagios can also use the result of the plugins that determine the present status of host or services of the network.</p>

<p align="justify">Now an answer to the questions that why we need plugins, you can also add here that, plugins is executed by Nagios to check the status of any service or host. A check is performed by the plugin and the result is returned to Nagios. The result is processed by Nagios to take the necessary actions.</p>
</details>

<details>
<summary><b>What do you understand by NRPE or Nagios Remote Plugin Executor of Nagios?</b></summary><br>
<p align="justify"><b>NRPE</b> or <b>Nagios remote plugin executor</b> is designed to allow execution of plugins on remote Linux or UNIX based machines. These plugins are executed to monitor the usage of CPU load and memory usage like a local resource of remote machines. It is required as this information is not usually exposed publicly to an external machine and for this purpose, <b>NRPE agent</b> is installed on remote machines.</p>

<b>NRPE add-on</b> or plugin has two components that work together to perform the task:

A ‘<b>check_nrpe</b>’ plugin that resides on the local machine and it is used for monitoring
The <b>NRPE daemon</b> that can run on remote machines
</details>

<details>

<summary><b>What are port numbers used by Nagios for monitoring purpose?</b></summary><br>
Usually, the port number <b>5666</b>, <b>5667</b> and <b>5668</b> are used for monitoring in Nagios.
</details>

<details>
<summary><b>Explain main configuration file and its location.</b></summary><br>
Following is the description of the main configuration file:

<ul>

<li><b>Resource File:</b> To store sensitive information like user details that may include username and passwords it is used. The information is not made available to CGI.</li>

<li><b>Object Definition File:</b>  In this file, you can find and enlist the details of resources that you want to monitor and how you want the monitoring to be performed? Host services, host groups, contacts, contact groups, commands, etc. are defined in this file.</li>

<li><b>CGI Configuration File:</b> Several directives are contained and stored in CGI file that can affect the CGI o. A reference to the main configuration file is also stored in this file, so that CGI can know the details of Nagios configuration as and when required and the location of object definition storage.</li>
</ul>
</details>

<details>
<summary><b>What are state types of Nagios?</b></summary><br>
Following are the state types of Nagios:
<ul>
<li>Service or host state type.</li>
<li>Some states like <b>OK</b>, <b>WARNING</b>, <b>UP</b>, or <b>DOWN</b> state host or service.</li>
<li>Two state types that are <b>SOFT</b> state or <b>HARD</b> state.</li>
</ul>
</details>

<details>
<summary><b>What are SOFT and HARD states?</b></summary><br>
We can define soft and hard states as:

<p align="justify">In case of the SOFT state, the service or host check results are not OK or not up to the mark, even in case if service check has not been rechecked the number of times that are specified for it moreover the times that is being specified by the max_check_attempts directive. Recovery of the component from such Soft error is called Soft Recovery.</p>
<p align="justify">When a host or service check result is not ‘OK’ and it has been checked for the number of times, specified by the max_check_attempts directive in the host definition, then this error is known as Hard Error. Recovery of any service from this error is known as Hard Recovery.</p>
</details>

<details>
<summary><b>What is state stalking in Nagios?</b></summary><br>
<p align="justify">State stalking is used for logging purpose in Nagios. When stalking is enabled for any service or host then Nagios watch it very carefully and store any changes that if found in the check result of that resource.

Stalking can be helpful in later stages of log file analysis. Here in such scenario, any host or service check can be performed only if it has been updated for the last time.</p>
</details>

<details>
<summary><b>Why is it being said that Nagios is object oriented?</b></summary><br>
<p align="justify">Nagios has object configuration format where you can create object definitions, that can inherit the properties from other hostnames or object definitions. In this way, you can specify the component relationships easily. The components are considered as objects by the Nagios.</p>

</details>

<details>
<summary><b>Which three Nagios variables can affect recursion and inheritance in Nagios?</b></summary><br>
The three variables that affect recursion and inheritance are:
<ul>
<li>Name</li>
<li>Use</li>
<li>Register</li>
</ul>
<p align="justify">Here, Name is just a placeholder that can be used by the other objects. Use variable can be used to define parent object, whose properties are to be used. Registers are also used for storing values that can be either 0 or 1. Register values cannot be inherited.</p>
</details>

<details>
<summary><b>How Does Flap detection work in Nagios?</b></summary><br>
<p align="justify">When a service or host changes their state frequently, then it is called flapping that may cause lots of problems and generate too many recovery notifications. Flapping is detected in the following manner:</p>
<ol type="a">
<li>Store the results of last 21 checks and then analyze this historical check result to know the number of transitions that are being taken place by the host or service.</li>
<li>Know the percent state change value with the help of state transition.</li>
<li>Compare the value of this state change against low and high flapping thresholds.</li>
<li>When this value exceeds then the highest specified threshold then it is called flapping.</li>
<li>When this percent state value goes down the specified value then it is said that flapping has been stopped.</li>
</ol>
</details>

<details>
<summary><b>Explain main configuration file of Nagios.</b></summary><br>
<p align="justify">Several directives are contained in the main configuration file that can affect Nagios daemon. This file is read by both CGIs and Nagios daemons.</P>

<p align="justify">A Nagios file is usually created in the base Nagios directory, at the time when you run configuration script. The name of this file that is the main configuration file is ‘nagios.cfg’ and is usually placed in etc/subdirectory.</p>
</details>

<details>
<summary><b>How is distributed monitoring being done in Nagios?</b></summary><br>
<p align="justify">There is a distributed monitoring scheme in Nagios with the help of which you can monitor your complete enterprise that may include local slave instances. In such environment, Nagios submit the result of reports of tasks to a single machine. All configuration, reporting, and notification can be managed at the master machine and here slaves do all the work. Here Nagios uses passive checks that are basically external applications that can send the results back to Nagios.</p>
</details>

<details>
<summary><b>Differentiate between active and passive check.</b></summary><br>
<p align="justify">The major difference between active and passive check is that Active checks are initiated by Nagios itself, while Passive checks are performed by external applications.</p>
</details>

## <a name="Questions-1">Others</a>

***
<p align="center">
  <sub>Created by
  <a href="dolbyjoab.github.io">Etienne</a> and
  <a href="https://github.com/dolbyjoab/101-nagios/graphs/contributors">
    contributors
  </a>
    </sub>
</p>
