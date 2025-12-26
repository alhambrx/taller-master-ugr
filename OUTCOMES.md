# Exercise Outcomes Submission Template

**Student/Group Name**: Alhambra Espigares
**Level Completed**: newbie
**Date**: 26-12-2025

---

## 📋 Exercise Summary

### Exercise: Newbie Level
**Status**: ✅ Completed 

**What I did**:
Complete el ejercicio de nivel Newbie practicando los fundamentos de Git. Configure mi identidad en Git, clone el repositorio usando SSH, cree un archivo `hello.txt` con mi nombre, lo anadi al area de staging y lo confirme con un commit, y revise el historial de commits. Luego, cree la rama `feature/my-info`, anadi un archivo `my-info.txt` con mi informacion personal y mis preferencias de programacion, hice commit de los cambios y subi la rama a mi fork. Finalmente, cree la rama de resultados `alh-outcomes/newbie` y documente todos los comandos, salidas, desafios y reflexiones en OUTCOMES.md.


**Commands Used**:
```bash
# List the key Git commands 
git config --global user.name "alhambrx"
git config --global user.email "alhambraespigares@gmail.com"
git clone git@github.com:alhambrx/taller-master-ugr.git
git checkout -b newbie origin/newbie
git status
git add hello.txt
git commit -m "Add hello.txt with my name"
git log
git checkout -b feature/my-info
git add my-info.txt
git commit -m "Add personal information"
git push origin feature/my-info
```

**Results/Output**:
```
Switched to a new branch 'feature/my-info'

Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 619 bytes | 103.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'feature/my-info' on GitHub by visiting:
remote:      https://github.com/alhambrx/taller-master-ugr/pull/new/feature/my-info
remote:
To https://github.com/alhambrx/taller-master-ugr.git
 * [new branch]      feature/my-info -> feature/my-info
```

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. Crear y cambiar entre ramas locales.
2. Diferencia entre repositorios locales y remotos.
3. Flujo basico de add - commit - push.

**Skills I improved**:
- Hacer commits claros.
- Ver historial de commits con git log.
- Trabajar con ramas y remoto.

---

## 🚧 Challenges Faced

### Challenge 1: SSH push denied
**Problem**: Al principio intente hacer push a origin/main y me salio error 403.
**Solution**: Hice un fork de repositorio y use SSH para clonar mi fork. Luego pude hacer push sin problemas.
**Commands/Approach**:
git clone git@github.com:alhambrx/taller-master-ugr.git
git push origin feature/my-info

---

## 💭 Personal Reflection

**What surprised me**:
El modo de funcionar cada rama de manera independiente
**What I found most difficult**:
Saber en cada paso en que rama me encuentro para hacer los cambios en la adecuada
**What I found most useful**:
La organizacion
**How I would apply this in real projects**:
Siempre crear una rama para cada feature y documentar commits claros
---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | 5 | Me siento comoda con los comandos basicos |
| Branching & merging | 4 | Puedo crear y moverme entre ramas|
| Remote operations | 3 | Entiendo la importancia de ir haciendo push y pull |
| Conflict resolution | 2 | No he trabajado conflictos de momento |
| History rewriting | 2 | No lo he puesto en practica en este ejercicio|
| Git hooks | 1 | No lo he usado todavia |
| Security practices | 3 | Configuramos SSH|

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/alhambrx/taller-master-ugr/tree/alh-outcomes/newbie`
- Key commits demonstrating your work:
  - 3f4467b: Add hello.txt with my name
  - 173e46a: Add personal information

**Additional files created** (if any):
- hello.txt
- my-info.txt

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [ ] Completed the exercise for your chosen level (including all parts)
- [ ] Documented all commands used with their outputs
- [ ] Described challenges and how you resolved them
- [ ] Provided a thoughtful reflection on your learning
- [ ] Self-assessed your confidence in each topic
- [ ] Pushed your outcome branch to the remote repository
- [ ] Created a Pull Request (if required by your instructor)

---

**Submission Date**: 26-12-2025  
**Ready for Review**: ✅ Yes 
