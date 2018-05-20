# HLS.Download
C# HLS (m3u8) library to parse HLS streams and adaptive HLS stream lists

# Functions:
* Parse HLS streams and adaptive HLS stream lists straight from file or piece of text;
* (Todo) Download HLS streams to playable files;
* (Todo [probably not going to be added]) Create HLS streams and adaptive HLS stream lists (with optional key.)

# Example class demonstration
```
using HLS.Download.Models;

class ConsoleApp1
{
  static async Task Main(string[] args)
  {
    HLSStreamEntry[] streams = HLSStreamEntry.Parse(args[0]);
    HLSStream stream = await HLSStream.Open(streams[0].Path);
    
    Console.WriteLine(stream.TargetDuration);
  }
}
```
