Requires passlib i.e pip install passlib

ansible-galaxy install -r requirements.yaml --force

ansible-playbook -i ./inventory.yaml dummy.yml 