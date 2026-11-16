- `EDEN_NX2_NCE_REPORT=1` (diagnostic): one log line per module a game loads, on any host, with
  what native code execution (NCE) on ARM64 hosts would rewrite and which system registers it
  would leave to the host CPU, so Switch 2 titles can be checked for NCE without an ARM64 device.
  [docs/NCE.md](docs/NCE.md) has the plan for NCE on Linux ARM64, Android, Windows on ARM and macOS.
