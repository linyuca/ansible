initial setup: following two files need to becreated at current dir
   create ansible.cfg
   vnf

1) ncs clean up 
   ansible-playbook sae_clean_up.yaml                     # run all task
   ansible-playbook sae_clean_up.yaml --tags stitching    # run only stitching task
   ansible-playbook -vvv sae_clean_up.yaml                # run with debug information
   or
   ansible-playbook sae_clean_up.yaml -i /path-to/inv     # tell teh ansible where is the inventory file

    
2) ansible esc -a "health.sh"
   ansible esc -a "esc_nc_cli get esc_datamodel/opdata"
 
3) ansible n9k -m raw -a "sh ip int bri" 
   ansible n9k -m raw -a "sh lld neig"
