# SALA VERMELHA — PWA MVP v0.1

## Incluído
- Catálogo com 150 entradas numeradas e filtros.
- Dois modos: quiz e simulação sequencial.
- Consulta de dados do paciente por painéis expansíveis.
- Feedback imediato após cada alternativa, com justificativa individual e explicação da resposta correta.
- Progresso salvo localmente no navegador.
- Manifest e service worker para instalação como PWA e cache offline após primeiro acesso.

## Limitações importantes
- As 150 entradas são derivadas de **30 cenários-base** com repetição/variações de apresentação, não 150 casos originais. As variantes não representam complexidade médica adicional real, embora estejam classificadas em 5 níveis para prototipação da interface.
- A simulação é sequencial e **não** ramifica sinais vitais ou desfechos conforme as decisões. Isso requer autoria clínica específica.
- Material **não validado clinicamente**, apenas protótipo educacional; não usar como protocolo assistencial nem avaliação formal.
- Dados ficam no localStorage do aparelho, sem login nem sincronização.

## Testar no computador
Na pasta do projeto, execute:

```bash
python3 -m http.server 8000
```

Abra http://localhost:8000

## Publicar na Cloudflare Pages
Crie um projeto Pages e envie os arquivos estáticos da pasta `sala-vermelha` (index.html, app.js, cases.json, manifest.webmanifest, icon.svg, sw.js). Não é necessário build. Também é possível usar GitHub conectado ao Pages com comando de build vazio e diretório de saída `/`.

## Instalar no iPhone
Após publicar em HTTPS, abra o site no Safari → Compartilhar → Adicionar à Tela de Início.

## Próximos passos
1. Substituir cenários repetidos por 150 casos originais de dificuldade crescente, com revisão médica e fontes.
2. Criar árvore de decisões por caso, com evolução clínica coerente e desfechos condicionais.
3. Implementar etapas, múltiplas perguntas e pontuação por competência.
4. Testes clínicos e de acessibilidade.


## v0.3
- 1.000 posições, paginação de 100, filtros, pontuação por acerto e 12 ilustrações temáticas reutilizáveis.
- Importante: os 1.000 registros NÃO representam 1.000 casos originais. Os 150 cenários anteriores são reutilizados em variantes de treino e exigem revisão clínica.
- As ilustrações são decorativas e não devem ser interpretadas como exames do paciente.
