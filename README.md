# sqwatch 🖥️

A lightweight terminal tool to monitor SLURM GPU partition queues. Helps you find the shortest queue to submit your jobs.

![Demo](demo.png)

## Features

- 📊 **Sorted by queue length** - Shortest queues shown first
- 🔍 **Auto-detect GPU partitions** - Works out of the box
- 👤 **Shows your jobs** - See your running/pending jobs
- 💡 **Recommendations** - Instantly know where to submit
- ⚡ **Zero dependencies** - Pure Python 3, no pip install needed

## Install

```bash
# Clone
git clone https://github.com/YOUR_USERNAME/slurm-queue-watch.git
cd slurm-queue-watch

# Make executable
chmod +x sqwatch

# Run
./sqwatch
```

Or just copy the single file:

```bash
curl -O https://raw.githubusercontent.com/YOUR_USERNAME/slurm-queue-watch/main/sqwatch
chmod +x sqwatch
./sqwatch
```

## Usage

```bash
./sqwatch              # Monitor with 5s refresh
./sqwatch -i 3         # Refresh every 3 seconds
./sqwatch -1           # Run once and exit
./sqwatch -p gpu,gpu_requeue  # Monitor specific partitions
```

Press `Ctrl+C` to exit.

## How It Works

Uses standard SLURM commands (`squeue`, `sinfo`) to collect queue statistics. No special permissions required - if you can run `squeue`, you can use this tool.

## Compatibility

Works on any SLURM cluster. Tested on:
- Harvard FASRC
- (Add your cluster here via PR!)

## License

MIT

