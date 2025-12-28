git add .
git commit -m "Update notes"
for i in {1..25}
do
  echo "Commit number $i" >> progress.txt
  git add progress.txt
  git commit -m "Progress update $i"
done
