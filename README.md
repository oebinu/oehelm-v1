# oehelm-v1

git clone https://github.com/oebinu/oehelm-v1.git
mkdir test
helm pull argo/argo-cd
mv argo-cd-5.52.1.tgz test
helm repo index test
git add ./
git commit -am "2024.01.09 Test Helm Repo(1)"
git push
helm repo add github-stable https://oebinu.github.io/oehelm-v1/



helm repo index docs
git commit -am "2024.01.09 Test Helm Repo(3)"
git push


helm repo index docs --url https://oebinu.github.io/oehelm-v1/
git commit -am "2024.01.09 Test Helm Repo(4c)"
git push


helm repo add oehelm https://oebinu.github.io/oehelm-v1/

helm package oebinu-db 
helm package oebinu-web 
mv *.tgz ../docs

helm repo index docs --url https://oebinu.github.io/oehelm-v1/
git add ./ && git commit -am "2024.01.10" && git push

helm repo update
helm search repo oehelm 
helm repo remove oehelm 
helm repo add oehelm https://oebinu.github.io/oehelm-v1/
