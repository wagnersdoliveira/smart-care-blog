---
layout: post
title: "Como conferir atualizações de programas no Windows com winget"
date: 2026-10-17
category: Softwares
description: "Use o Gerenciador de Pacotes do Windows para verificar atualizações antes de instalar."
reading_time: 4
image: /assets/images/laptop-maintenance.jpg
image_alt: "Área de trabalho preparada para manutenção de um notebook"
image_caption: "Área preparada para manutenção de notebook"
image_credit: "Giorgio Malvone"
image_source: "https://commons.wikimedia.org/wiki/File:Laptop_Maintenance_Work_Area.jpg"
---

Manter os programas atualizados ajuda a receber correções e melhorias. No Windows, o `winget` pode procurar atualizações disponíveis para muitos aplicativos.

## 1. Confira se o winget está instalado

Abra o **Terminal** ou o **PowerShell** e execute:

```powershell
winget --version
```

Se o comando não for reconhecido, procure por **Instalador de Aplicativo** na Microsoft Store e instale ou atualize o pacote oficial da Microsoft.

## 2. Veja quais programas têm atualização

```powershell
winget upgrade
```

Leia a lista antes de continuar. O resultado depende dos programas instalados e das fontes configuradas no computador.

## 3. Atualize um programa específico

Use o identificador exibido na lista:

```powershell
winget upgrade --id Microsoft.PowerToys
```

Troque `Microsoft.PowerToys` pelo identificador do programa que você conferiu. Revise as opções de instalação apresentadas e feche o aplicativo antes de atualizar, se necessário.

## E para atualizar tudo?

O comando abaixo tenta atualizar todos os pacotes reconhecidos:

```powershell
winget upgrade --all
```

Use-o somente depois de revisar a lista. Alguns aplicativos podem exigir etapas próprias, reinicialização ou confirmação de licenças. Evite automatizar a atualização de todos os programas sem entender o impacto no seu computador.

> Dica: faça backup dos arquivos importantes e mantenha o Windows atualizado pelo Windows Update. O `winget` complementa esse processo, mas não substitui atualizações do sistema.
