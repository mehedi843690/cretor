git add .
git commit -m "Update notes"
for i in {1..25}
do
  echo "Backdated commit $i" >> history.txt
  git add history.txt
  GIT_AUTHOR_DATE="2025-01-$i 12:00:00" \
  GIT_COMMITTER_DATE="2025-01-$i 12:00:00" \
  git commit -m "Backdated commit $i"
done
git push origin main
