- Stop: each teardown step is logged with its time (`Shutdown step N took X ms: <step>`), the last
  line names the slowest, and the stop watchdog's lines name the last step done, so a slow stop
  says where its time went ([#239](https://github.com/karimalsalah/guarana/issues/239)).
- Stop: a teardown busy on the CPU is no longer taken for a hung one. After a long session the
  watchdog could end the program during a step that works without noting progress, and a Stop
  from the menu then closed the whole app instead of going back to the game list. Compute
  pipelines are destroyed with progress, like the graphics ones
  ([#239](https://github.com/karimalsalah/guarana/issues/239)).
- Stop: the Windows trim of all-zero guest memory pages stops when a Switch 2 game stops, and a
  pass in progress ends at its next check: a stop could wait for a whole pass over memory it
  was about to release ([#239](https://github.com/karimalsalah/guarana/issues/239)).
