# Relatório do Projeto -- Gerenciamento de Arquivos e Permissões

## 📌 Projeto

Este projeto tem como objetivo compreender e aplicar **operações de
gerenciamento de arquivos e controle de permissões** nos sistemas
operacionais **Windows, Linux e Android**.\
Foram exploradas ferramentas nativas de cada sistema, como `chmod`,
`icacls` e `adb shell`, permitindo comparar os diferentes modelos de
segurança, acesso e estrutura de diretórios.

O estudo foi desenvolvido na disciplina **Sistemas Operacionais**, sob
orientação do professor **Clóvis Ferraro**.

------------------------------------------------------------------------

## 📖 Conteúdo

1.  Introdução\
2.  Metodologia\
3.  Linux -- Gerenciamento de Permissões\
4.  Windows -- Controle de Acesso com ACLs\
5.  Android -- Gerenciamento via ADB\
6.  Comparação e Análise Crítica\
7.  Discussão\
8.  Conclusão\
9.  Referências

------------------------------------------------------------------------

## 🐧 Linux -- Gerenciamento de Permissões

No Linux, as permissões são baseadas em três classes de acesso:
**dono**, **grupo** e **outros**.\
Foram utilizados comandos como:

``` bash
mkdir projetos
touch grupo10p2.txt
chmod 600 grupo10p2.txt
sudo chown root:root grupo10p2.txt
ln -s grupo10p2.txt link_arquivo_grupo10p2
df -h
file grupo10p2.txt
```

➡ Esses comandos permitiram criar pastas, arquivos, modificar donos e
permissões, além de identificar tipos de arquivo e monitorar o uso de
disco.

------------------------------------------------------------------------

## 🪟 Windows -- Controle de Acesso com ICACLS e FSUTIL

O Windows utiliza o sistema **NTFS**, que trabalha com **Listas de
Controle de Acesso (ACLs)**.\
As ferramentas utilizadas foram:

``` bat
icacls C:\Windows\* /save AclFile /T
fsutil volume diskFree C:
```

➡ O `icacls` permite salvar, aplicar e restaurar permissões detalhadas
de arquivos e pastas.\
➡ O `fsutil` foi usado para gerenciar volumes e verificar o espaço livre
em disco.

------------------------------------------------------------------------

## 🤖 Android -- Acesso via ADB Shell

No Android, as permissões seguem a estrutura do **Linux**, mas com
**isolamento de aplicativos** através de UIDs e SELinux.\
Com o `adb shell`, foram executados comandos como:

``` bash
ls -l /data/data/com.example.app
chmod 700 arquivo.txt
```

➡ Cada aplicativo possui um identificador exclusivo (UID), garantindo
que um app não acesse arquivos de outro, reforçando a segurança do
sistema.

------------------------------------------------------------------------

## 📊 Comparação e Análise Crítica

  --------------------------------------------------------------------------------------
  Sistema       Ferramentas     Filosofia de Permissão      Nível de    Resumo Crítico
                                                            Controle    
  ------------- --------------- --------------------------- ----------- ----------------
  **Linux**     `chmod`,        Numérica (r, w, x) por      Média a     Flexível e
                `chown`         dono, grupo e outros        Alta        eficaz, mas
                                                                        requer
                                                                        conhecimento
                                                                        técnico.

  **Windows**   `icacls`, NTFS  ACLs detalhadas             Alta        Controle
                                                                        preciso, ideal
                                                                        para ambientes
                                                                        corporativos.

  **Android**   `adb`,          Isolamento por UID e        Baixa a     Prioriza
                permissões por  SELinux                     Média       segurança, com
                app                                                     menor
                                                                        flexibilidade.
  --------------------------------------------------------------------------------------

➡ Cada sistema reflete uma filosofia distinta: **Linux** prioriza o
controle técnico, **Windows** o equilíbrio entre usabilidade e
segurança, e **Android** o isolamento máximo para proteger o usuário.

------------------------------------------------------------------------

## ✅ Conclusão

Foi possível compreender que o gerenciamento de arquivos e permissões é
essencial para garantir segurança e organização nos sistemas
operacionais.\
- O **Linux** oferece flexibilidade e domínio total ao usuário.\
- O **Windows** apresenta controle granular com ACLs.\
- O **Android** foca na proteção, isolando processos e aplicativos.

O projeto consolidou o entendimento prático sobre como as permissões
afetam o acesso, a segurança e a integridade dos dados em diferentes
ambientes.

------------------------------------------------------------------------

## 👨‍💻 Grupo

-   [Damião Junior](https://github.com/juninho-Oliveira)\
-   [Luigi Borges Locatelli](https://github.com/Luigi-Loc)\
-   [Otavio Henrique Azevedo Chaves](https://github.com/OtavioHx0)\
-   [Pedro Henrique Sales Siquele](https://github.com/TheBestOFWord)
