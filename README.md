# vscode_debug_scripts
VSCode Debug Python(Pytest) code + CPP code launch.json
<code json>
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "type": "lldb",
            "request": "attach",
            "name": "Attach",
            "pid": "${command:pickMyProcess}", // use ${command:pickProcess} to pick other users' processes
        },
        {
            "name": "EthosnConv2d",
            "type": "python",
            "request": "launch",
            "stopOnEntry": false,
            "module": "pytest",
            "args": [
                "-sv",
                "--disable-pytest-warnings",
            ],
            "env": {},
            "envFile": "${workspaceRoot}/.env",
            "cwd": "/home/radar/code/tvm/tests/python/contrib/test_ethosn/test_conv2d",    //pytest要运行的脚本路径
            //"preLaunchTask": "enable_ptrace_scope"
        }
    ],
}
  
</code>
