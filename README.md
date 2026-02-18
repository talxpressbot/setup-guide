# mac setup guide

Step 0) Wipe hard drive (add instructions for that)

Then update MacOS to newest version.

Install node.js from downloadable installer.

Make sure to add bin to $PATH:
```
echo "export PATH=\"$BIN_PATH:\$PATH\"" >> ~/.zshrc 
```

Might need to do this also (If getting EACCESS errors)
```
sudo chown -R $(whoami) /usr/local/lib/node_modules
```

# Installing Openclaw
```
npm i -g openclaw
```



# Running Openclaw
```
openclaw onboard --install-daemon
```


I like to choose these options for ollama setup:

1) Continue: Yes

2) Onboarding mode: Quickstart

3) Model/auth provider: Skip for now

4) Filter models by provider: All providers

5) Default model: Keep current  (Doesn't really matter since we're gonna change it to ollama right away)

6) Select channel (QuickStart): WhatsApp (QR link)

7) Link WhatsApp now (QR): Yes

- Scan the QR Code (in what's app camera, not regular iphone camera)

- Check that is says ✅ Linked after restart; web session ready.

8) WhatsApp phone setup: This is my personal phone number

9) Number: [enter number]

10) Configure skills now? (recommended): No

11)  Enable hooks: Skip for now

12) How do you want to hatch your bot: Hatch in TUI (recommended)





## Brew install

(Because Ollama installed through brew seemed to work best for me)

install with brew from: https://brew.sh/

make sure to run the commands at the end.


## Ollama Install

```brew install ollama```


✅ 1️⃣ Start Ollama
ollama serve


(Leave it running in that terminal.)

In another terminal, you can interact with it.

✅ 2️⃣ List Installed Models
ollama list


If it’s fresh, you’ll probably see nothing.

✅ 3️⃣ See Available Models (Remote Library)

You can search:

ollama search qwen


Or browse:

👉 https://ollama.com/library


```
ollama pull qwen2.5-coder:7b
```

✅ 5️⃣ Test It
ollama run qwen2.5-coder:7b


Type something and make sure it responds.

Exit with:

```
/bye
```



