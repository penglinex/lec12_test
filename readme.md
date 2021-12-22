Леонович Артём Игоревич
Очистка мусора производилась с помощью git filter-branch
Папка с изображениями была удалена с помощью команды git filter-branch --tree-filter 'rm -f images/*.jpg' HEAD
Папка folder1 была удалена с помощью команды git filter-branch --tree-filter 'rm -rf folder1’ HEAD
Очистка мусора git reflog expire --expire=now --all && git gc --prune=now --aggressive
Обновление истории веток и тегов git push origin --force --all и git push origin --force –tags
Для удаления копий была использована команда git filter-branch --force --tree-filter 'rm -f "ssh3 — копия.txt"' HEAD и git filter-branch --force --tree-filter 'rm -f "ssh — копия.txt"' HEAD