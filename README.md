### Supprimer toutes les branches en local non présentes sur le remote
```bash
git fetch -p && for branch in $(git branch -vv | grep ': gone]' | awk '{print $1}'); do git branch -D $branch; done
```
