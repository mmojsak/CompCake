---
layout: default
---

#  CompCake

The cake fairy has chosen:
  -  Name1
  -  Name2
  -  Name3
    
To bring the cake next week, see you all on the 26th!


<script src="https://pyodide-cdn2.iodide.io/v0.18.1/full/pyodide.js"></script>
<script>
  async function runPython() {
    let pyodide = await loadPyodide();
    let code = document.getElementById("python-code").value;
    let output = await pyodide.runPythonAsync(code);
    document.getElementById("output").innerText = output;
  }
</script>

<textarea id="python-code">print("Hello from Pyodide!")</textarea>
<button onclick="runPython()">Run</button>
<pre id="output"></pre>
