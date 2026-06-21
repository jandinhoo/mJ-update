# Skill Field Mapping

Gerado em: `2026-05-16T10:14:03`

## Fontes usadas

- Cache main-db validado: `D:\Zcodex\DecayTools\SkillEditorCache\main-db\66E6992DC5038E9F2BAF56184A9614ED31F607F92A30103DD540D42CB6E33F70.json` entries=139999
- Cache nativo `.so`: `D:\Zcodex\DecayTools\SkillEditorCache\1C9204CD92B16241E39763A0A0DFC53D01C5378435CF542BF634AF9DCAA3BD22.json` entries=260137
- O cache main-db valida o offset comparando contexto de bytes contra o `libskill.so` atual antes de liberar escrita.

## Totais

- mapped_methods: `487`
- legacy_field_records: `139999`
- high_confidence: `424`
- medium_confidence: `12`
- lua_only: `4`
- low_confidence: `47`
- promoted_from_low_by_validated_main_cache: `316`

## Regra de confian?a

- `Alta`: patch nativo no `.so` ou offset do `main/skill.db` validado por contexto contra o `libskill.so` atual.
- `Media`: existe no `.so` ou em fonte parcial, mas ainda precisa correla??o/teste por skill.
- `Lua somente`: existe nos scripts, sem patch server-side conhecido.
- `Baixa`: pista isolada de estrutura/Lua/main sem offset validado; n?o deve ser prometida como edi??o funcional.

## Promovidos

Os `State.Set*` abaixo deixaram de ser baixa confian?a porque agora possuem offsets do `main/skill.db` validados no `.so` atual.

| Campo | Humano | Categoria | Cache validado | Skills |
|---|---|---|---:|---:|
| `State.SetProbability` | Estado - Chance | Estados | 1003 | 475 |
| `State.SetTime` | Estado - Duracao | Tempo | 966 | 473 |
| `State.SetPerform` | Estado - Perform/animacao | Estados | 763 | 579 |
| `State.SetValue` | Estado - Valor/intensidade | Estados | 740 | 408 |
| `State.SetRatio` | Estado - Multiplicador | Estados | 693 | 395 |
| `State.SetBuffid` | Estado - Buff/efeito ID | Estados | 617 | 376 |
| `State.SetPray` | Estado - Preparacao | Estados | 517 | 517 |
| `State.SetAmount` | Estado - Quantidade/intensidade | Estados | 492 | 321 |
| `State.SetVar1` | Estado - Variavel 1 | Estados | 282 | 171 |
| `State.SetVar2` | Estado - Variavel 2 | Estados | 120 | 63 |
| `State.SetVar3` | Estado - Variavel 3 | Estados | 57 | 28 |
| `State.SetDispel` | Estado - Dispel | Estados | 56 | 48 |
| `State.SetSlow` | Estado - Lentidao | Estados | 47 | 47 |
| `State.SetClearcooldown` | Estado - Limpar cooldown | Tempo | 38 | 25 |
| `State.SetHpleak` | Estado - Dreno de HP | Estados | 37 | 36 |
| `State.SetPasaddsmite` | Estado - Passivo adiciona smite | Estados | 33 | 33 |
| `State.SetHeal` | Estado - Cura | Estados | 30 | 30 |
| `State.SetSilent` | Estado - Silencio | Estados | 27 | 27 |
| `State.SetSetcooldown` | Estado - Definir cooldown | Tempo | 26 | 23 |
| `State.SetAddspeed` | Estado - Velocidade extra | Estados | 25 | 24 |
| `State.SetPasaddhp` | Estado - Passivo adiciona hp | Estados | 25 | 25 |
| `State.SetWeak` | Estado - Fraqueza | Estados | 24 | 24 |
| `State.SetCleardebuff` | Estado - Limpar debuff | Estados | 23 | 22 |
| `State.SetPasaddattack` | Estado - Passivo adiciona attack | Estados | 22 | 22 |
| `State.SetDizzy` | Estado - Atordoar | Estados | 21 | 21 |
| `State.SetIncattack` | Estado - Aumentar ataque | Estados | 21 | 21 |
| `State.SetWrap` | Estado - Prender | Estados | 21 | 21 |
| `State.SetPasadddefence` | Estado - Passivo adiciona defence | Estados | 20 | 20 |
| `State.SetDelaycast` | Estado - Atrasar cast | Tempo | 20 | 20 |
| `State.SetDirecthurt` | Estado - Dano direto | Estados | 19 | 19 |
| `State.SetPasaddmp` | Estado - Passivo adiciona mp | Estados | 19 | 18 |
| `State.SetVar4` | Estado - Variavel 4 | Estados | 19 | 15 |
| `State.SetCreateobject` | Estado - Criar objeto | Estados | 16 | 9 |
| `State.SetDodge` | Estado - Esquiva | Estados | 16 | 16 |
| `State.SetPasaddsilent` | Estado - Passivo adiciona silent | Estados | 16 | 16 |
| `State.SetPasinccrit` | Estado - Passivo aumenta crit | Estados | 16 | 16 |
| `State.SetDecdefence` | Estado - Reduzir defesa | Estados | 15 | 15 |
| `State.SetPasadddizzy` | Estado - Passivo adiciona dizzy | Estados | 15 | 15 |
| `State.SetEvilaura` | Estado - Evilaura | Estados | 14 | 14 |
| `State.SetHpgen` | Estado - Regeneracao HP | Estados | 14 | 13 |

## Baixa restante

Estes campos ainda n?o foram promovidos porque n?o h? patch nativo, cache main-db validado nem Lua edit?vel confirmando o comportamento.

| Campo | Categoria | Ind?cio atual | Pr?xima prova necess?ria |
|---|---|---|---|
| `DistanceFormula` | Alcance | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.castdistance` | Alcance | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.cminpray_distance` | Alcance | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.cylinderradius` | Alcance | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.pursue_distance` | Alcance | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.radius` | Alcance | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.sectorangle` | Alcance | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.sectorradius` | Alcance | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `getpraydistance` | Alcance | nenhum offset validado | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `Calculate` | Combate | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.other_ratio` | Combate | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `GetXpcost` | Custos | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `BuffFormula` | Estados | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.statecondition` | Estados | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `StateAttack` | Estados | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `blessme` | Estados | nenhum offset validado | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `takeeffect` | Estados | nenhum offset validado | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `GetGoodsid` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `GetGroupcdid` | Sistema | estrutura:2 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `GetProcedureCombo` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `GetProcedureNum` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `GetShapeLimit` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.ID` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.ap_cost` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.campGfxType` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.cylinderlength` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.energy1_cost` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.energy2_cost` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.ep_cost` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.goods_id` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.goods_num` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.groupcd_id` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.instanteGfx_Id` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.mapusable` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.movefix` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.mp_cost` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.procedure_num` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.shape_limit` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.soulskilltype` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.vp_cost` | Sistema | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `GetProcedureTime` | Tempo | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `GetTime` | Tempo | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.cooldown_time` | Tempo | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.execute_time` | Tempo | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.groupcd_time` | Tempo | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.movedelay` | Tempo | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |
| `SkillStub.showCampGfxTime` | Tempo | estrutura:1 | localizar offset real no `.so` ou Lua edit?vel vinculado |

## Arquivos

- `skill_field_map.json`: mapa completo para o editor consumir.
- `skill_field_map.csv`: mesma informa??o em planilha.
- `mapping_manifest.json`: hashes e fontes usadas.
