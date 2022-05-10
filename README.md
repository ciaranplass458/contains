# contains
#include "jq.au3"  $data = FileRead("Test2.json")  _jqInit() $sCmdOutput = _jqExec($data, '.[] | (objects | select(.name | contains("Fox 2")) | ."x-update-channel-icon" = true) // . ')  ConsoleWrite($sCmdOutput)
