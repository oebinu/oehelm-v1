# oehelm-v1

git clone https://github.com/oebinu/oehelm-v1.git
mkdir test
helm pull argo/argo-cd
mv argo-cd-5.52.1.tgz test
helm repo index test
git commit -am "2024.01.09 Test Helm Repo(1)"
git push