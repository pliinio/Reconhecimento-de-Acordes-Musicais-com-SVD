# Reconhecimento de Acordes Musicais com SVD  

Este projeto implementa um sistema de **reconhecimento automático de acordes musicais** a partir de arquivos de áudio no formato `.wav`.  
Utilizando técnicas de **Processamento Digital de Sinais (PDS)** e **Álgebra Linear**, o sistema extrai assinaturas espectrais com **Decomposição em Valores Singulares (SVD)** e classifica acordes com base na **similaridade cosseno**.  

---

## Funcionalidades  
-  **Remoção de silêncio** e normalização automática do áudio.  
-  **Extração de assinaturas espectrais** via SVD.  
-  **Organização hierárquica de dados musicais** (maiores, menores, fundamentais e inversões).  
-  **Classificação por similaridade cosseno**, agrupando acordes por proximidade harmônica.  
-  Suporte a diferentes formatos de organização de diretórios de áudio.  

---

##  Tecnologias Utilizadas  
- **Python 3.10+**  
- **NumPy** – operações matriciais  
- **SciPy** – leitura de áudio e STFT  
- **scikit-learn** – cálculo de similaridade  
- **OS / pathlib** – manipulação de diretórios e arquivos  

---

##  Estrutura de Diretórios  
```bash
acordes/
│
├── maiores/
│   ├── A/
│   │   ├── fundamental/
│   │   │   ├── arquivo1.wav
│   │   │   ├── arquivo2.wav
│   │   └── inversao1/
│   │       ├── arquivo3.wav
│   │
│   └── B/ ...
│
└── menores/
    └── C#/ ...
```

---

##  Como Executar  

1. Clone este repositório:  
   ```bash
   git clone https://github.com/pliinio/reconhecimento-acordes-svd.git
   cd reconhecimento-acordes-svd
   ```

2. Instale as dependências:  
   ```bash
   pip install -r requirements.txt
   ```

3. Ajuste o diretório base no código (`diretorio_base = "acordes"`) com seus arquivos `.wav`.  

4. Execute o script principal:  
   ```bash
   python main.py
   ```

---

##  Exemplo de Saída  
```bash
 Processando acorde A_maior...
 Assinatura extraída de arquivo1.wav
 Assinatura extraída de arquivo2.wav
...

 Similaridades com acordes conhecidos:
Acorde A_maior: Similaridade = 0.9521
Acorde C_menor: Similaridade = 0.7123
...

 Acorde classificado: A_maior
```

---

##  Possíveis Extensões  
- Implementar rede neural para classificação supervisionada.  
- Adicionar suporte a escalas e modos musicais.  
- Desenvolver interface gráfica para visualização dos espectros.  

---

##  Autor  
**Plinio Lima de Almeida Junior**  
-  Estudante de Engenharia de Computação – IFPB  
-  Músico e pesquisador em tecnologias musicais  
-  [GitHub](https://github.com/pliinio)  
