---
layout: post
title: "Um diagnóstico básico do Windows com PowerShell"
date: 2026-10-17
category: Manutenção
description: "Consulte informações do sistema e do disco sem alterar arquivos ou configurações."
reading_time: 3
image: /assets/images/computer-repair.jpg
image_alt: "Técnico realizando manutenção em um computador"
image_caption: "Manutenção de computador"
image_credit: "Vintechcomputerservices"
image_source: "https://commons.wikimedia.org/wiki/File:Computer_repair_in_progress.jpg"
---

Antes de procurar uma melhoria para o computador, é útil conhecer alguns dados básicos. Este exemplo apenas consulta informações: não instala programas, altera configurações ou apaga arquivos.

Abra o PowerShell e execute:

```powershell
$sistema = Get-CimInstance Win32_OperatingSystem
$disco = Get-CimInstance Win32_LogicalDisk -Filter "DeviceID='C:'"

[pscustomobject]@{
    Windows       = $sistema.Caption
    Versao         = $sistema.Version
    MemoriaLivreGB = [math]::Round($sistema.FreePhysicalMemory / 1MB, 1)
    EspacoLivreGB  = [math]::Round($disco.FreeSpace / 1GB, 1)
    DiscoTotalGB   = [math]::Round($disco.Size / 1GB, 1)
}
```

O resultado mostra a edição e a versão do Windows, além de uma estimativa da memória e do espaço livre no disco `C:`.

### Observações

- Se o Windows estiver instalado em outra unidade, ajuste `DeviceID='C:'`.
- A memória livre varia enquanto programas estão abertos.
- Compartilhe essas informações apenas com quem estiver ajudando no diagnóstico; elas podem identificar detalhes do seu computador.

Esse tipo de consulta é um primeiro passo. Se notar erros recorrentes, lentidão intensa ou pouco espaço livre, investigue a causa antes de executar scripts que façam alterações.
