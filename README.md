# subsquid-gorev

https://app.subsquid.io/network-dashboard giriş yaptıktan karşımıza görevler gelecektir.(gelmediyse sağ üstten "Switch to network" diyelim.)


`Terminalimizi açıyoruz. (Sunucumuza key yükeleyeceğiz Mobax öneririm kolaylık sağlar.)`

`Sırası ile komutlar:`

```console
npm install --global @subsquid/cli@latest

```

`-version kotrol edelim `
```console

sqd --version
```

yanıt olarak benzeri vermeli. => `@subsquid/cli/2.5.0 linux-x64 node-v20.5.1`




`-Klasör oluşturmak için devam edelim`

Klasör adını değiştirmek isterseniz `my-single-proc-squid`  2 yeri değiştirin.
```console
sqd init my-single-proc-squid -t https://github.com/subsquid-quests/single-chain-squid
cd my-single-proc-squid
```

Anahtar dosyasını bilgisayarımıza indirmek için görev kartındaki `Get key` basın. Ahatar dosyamız `singleProc.key` indirilecek, dosyamızı Mobax üzerinden `./query-gateway/keys` klasörüne süreki bırak yaparak kaydedip devam edelim. 

```console
sqd up

npm ci
sqd build
sqd migration:apply

sqd run .
```
`-Komut şuna benzer satırlar çıkarmalıdır:`

```console
[api] 09:56:02 WARN  sqd:graphql-server enabling dumb in-memory cache (size: 100mb, ttl: 1000ms, max-age: 1000ms)
[api] 09:56:02 INFO  sqd:graphql-server listening on port 4350
[processor] 09:56:04 INFO  sqd:processor processing blocks from 6000000
[processor] 09:56:05 INFO  sqd:processor using archive data source
[processor] 09:56:05 INFO  sqd:processor prometheus metrics are served at port 33097
[processor] 09:56:08 INFO  sqd:processor:mapping Burned 59865654 Gwei from 6000000 to 6016939
[processor] 09:56:08 INFO  sqd:processor 6016939 / 17743832, rate: 5506 blocks/sec, mapping: 304 blocks/sec, 182 items/sec, eta: 36m
```

10-15 dakika içinde senkronize olmasını bekleyelim.(Siteden kontrol edin) 

`-İşiniz bittiğinde Ctrl-C ile durdurma ve kaldırma işlemini yapalım.`
```console
sqd down

```

`Göre& Ödül Bilgisi`
| Category         | Skill Level                          | Time required (minutes) | Max Participants | Reward                              | Status |
| ---------------- | ------------------------------------ | ----------------------- | ---------------- | ----------------------------------- | ------ |
| Squid Deployment | $\textcolor{green}{\textsf{Simple}}$ | ~40                     | -                | $\textcolor{red}{\textsf{750tSQD}}$ | open   |
