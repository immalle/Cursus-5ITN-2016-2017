
# Wekker

Je hebt de namespace `System.Timers` nodig voor een timer.

```
class Wekker
{
	private Timer timer = new Timer();
	
	public Wekker(int hours, int minutes, int seconds) 
	{
		timer.Interval = seconds*1000 + minutes*60000 + hours*60000*60000;
		timer.Elapsed += timer_Elapsed;
	}
	
	public void Start()
	{
		timer.Start();
	}
	
	private void timer_Elapsed(object sender, ElapsedEventArgs e)
	{
		Console.WriteLine("TUDUDUDU TUDUDUDU TUDUDUDU");
		timer.Stop();
	}
}
```

Bij het gebruik van deze class in een Console-applicatie moet je wel de console 
laten wachten met Console.ReadLine(). Anders sluit de applicatie vroegtijdig af.



# Systeemgeluiden

Voor systeemgeluiden kan je deze code eens proberen:

```
using System.Media;
using System.Threading;

static void Main(string[] args)
	{
		SystemSounds.Beep.Play();
		Thread.Sleep(1000);
		SystemSounds.Beep.Play();
		Thread.Sleep(1000);
		SystemSounds.Beep.Play();
		System.Threading.Thread.Sleep(1000);
		SystemSounds.Beep.Play();
		System.Threading.Thread.Sleep(1000);
		SystemSounds.Asterisk.Play();
		System.Threading.Thread.Sleep(1000);
	}
```


# Speech synthesizer

De speech synthesizer zit in `System.Speech.Synthesis`. Je moet deze assembly eerst toevoegen aan je project.

Add Reference --> assemblies --> System.Speech.

Vervolgens zou deze code moeten werken:

```
using System.Speech.Synthesis;

namespace ConsoleApplication3
{
    class Program
    {
        static void Main(string[] args)
        {
            var synth = new SpeechSynthesizer();

            foreach (var voice in synth.GetInstalledVoices())
            {
                Console.WriteLine(voice.VoiceInfo.Name);
            }

            synth.Speak("sync sync sync sync sync"); // hierop wordt gewacht
            Console.WriteLine("SYNC CALL");
            
            synth.SpeakAsync("Async Async Async Async Async"); // hierop wordt niet gewacht, code gaat onmiddellijk verder
            Console.WriteLine("ASYNC CALL");
            Console.ReadLine();
        }
    }
}
```
