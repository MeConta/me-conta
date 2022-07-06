## 👣 Check in dance
Passos para atualizar as mudanças no github.

- Antes de tudo:

1. Garanta que está na pasta correta
```
cd <pasta>
```

2. Garanta que o git status está limpo

3. Faça o pull (base de código atualizada) 
```
git pull --rebase
```
4. Rode os testes
```
npm run test
```
5. Faça as alterações seguindo o TDD (red-green-refactor)

- Garanta que os testes estão passando:
```
npm run test
```
Se os testes falharem:

a) Corrija os testes com falha. 

b) Rode os testes novamente. 

c) Repita até que todos os testes estejam passando.

6. Commit localmente de acordo com o [padrão de mensagem](https://www.conventionalcommits.org/en/v1.0.0/): 

```
git add <arquivo> ou git add . 
git commit -m "<tipo(#código-tarefa): descrição>"
```

7. Faça o pull (base de código atualizada) 
```
git pull --rebase
```
Se houver conflitos, corrija os arquivos conflitantes e continue:
```
git add <arquivos> 
git rebase --continue
```
Se houve alterações, rode os testes novamente.

8. Push para repositório remoto 
```
git push
```
9. Após o push no submodulo, atualize o [repositório principal](https://github.com/MeConta/me-conta) de acordo com o check in dance.

10. Verifique o CI (verde). Caso a pipeline quebre (vermelho), faça as correções o quanto antes.