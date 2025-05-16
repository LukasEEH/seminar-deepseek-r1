# Ollama example

**Was ist Ollama?**

[Ollama](https://ollama.com) stellt eine Engine zur lokalen Ausführung von Quelloffenen LLMs bereit.

**Wie kann ich Ollama installieren?**

Um Ollama zu verwenden kann ein Downloader für die Engine über die entsprechende [Download Seite](https://ollama.com/download) heruntergeladen und installiert werden (verfügbar für MacOS, Linux, Windows)


**Wie verwende ich ein Modell lokal mit Ollama?**

Nach dem Download kann der Server mit `ollama serve` gestartet werden.

Über `ollama` können die **verfügbaren Aktionen** abgefragt werden:

```
~ % ollama 

Usage:
  ollama [flags]
  ollama [command]

Available Commands:
  serve       Start ollama
  create      Create a model from a Modelfile
  show        Show information for a model
  run         Run a model
  stop        Stop a running model
  pull        Pull a model from a registry
  push        Push a model to a registry
  list        List models
  ps          List running models
  cp          Copy a model
  rm          Remove a model
  help        Help about any command

Flags:
  -h, --help      help for ollama
  -v, --version   Show version information

Use "ollama [command] --help" for more information about a command.
```

Um ein DeepSeek-R1 Destillat zu verwenden kann das entsprechende model mit `ollama pull deepseek-r1:8b` (Die verfügbaren Destillate sind [hier](https://ollama.com/library/deepseek-r1) zu finden)

Nachdem ein Modell gepullt wurde, kann es mit `ollama run <model>` verwendet werden (Dafür muss der Ollama Server laufen).

Anschließend können beliebige prompts eingegeben werden:

```
~ % ollama run deepseek-r1:8b

>>> explain the GRPO algorithm

<think>
Okay, so I need to explain the GRPRO algorithm. 
Hmm, I'm not exactly sure ...
</think>

The GRPRO algorithm is designed for ...
```