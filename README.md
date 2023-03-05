# Reader-s-Writer-s-Pseudocode

Initialization:
  Semaphores:
    initial: 1
    control_writer: 0
    control_reader: 0
    write_mutex: 1
    exc: 1

  Variables:
    flag: 0
    writer_waiting: 0
    reader_waiting: 0
    switch: 0

Explanation:
1) Multiple readers can read together, while only 1 writer can write at once
2) Read and write operations are mutually exclusive
3) Switch from reader to writer or vice versa if the non-active process has atleast 1 waiting operation
4) This ensures that starvation is not possible
