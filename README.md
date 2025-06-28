# Super FX Assembly Help

This Visual Studio Code extension is a recreation of the Super FX (MARIO) code help parser BRIEF macro thing that Argonaut Software used while developing Star Fox 1/2.  

When a valid instruction is hovered over, it shows a tooltip box with info about the current instruction.  

<img src="./img/example.png" title="" alt="example.png" width="298">

This extension is currently only compatible with Argonaut's assemblers (SASM, ARGSFX, file extension *.MC) and Randal Linden's xAsm assembler (file extension *.a).  

## Compiling

Node.js, Git, and probably Visual Studio Code itself must be installed for this to compile. I don't know why Git is required, but it is.  
Open a PowerShell terminal window in the root of the repo and run ``npm install`` and ``npm install -g @vscode/vsce`` to setup all the dependencies.  
Run ``npm run compile`` to compile.  
Run ``vsce package`` to build a VSIX file that can be installed.  
Alternatively, use ``getmodules.cmd`` to install dependecies, use ``build.cmd`` to compile, and use ``package.cmd`` to make the VSIX file.

## TODO

- [ ] See if the "see also" instructions bit at the end can be made into hyperlinks to those instructions' explanations, or if a sort of interactive help directory thing can be added
- [ ] Add RAM and ROM cycle counts for every instruction (will take a long time)
- [ ] Add explanations for branch instructions (left out of the original)
- [ ] Detect Super FX code in xAsm source files properly (look for ``	cpu	sfx`` at beginning of file)