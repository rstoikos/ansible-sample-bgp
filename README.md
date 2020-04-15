# ansible-sample-bgp
ansible yaml files needed for basic bgp configuration


ansible.cfg = tell inventory to look local folder hosts file
group_vars =  variables that are common
host_vars = specific config for each host
templates/ios_bgp.j2 = jinja file for looping bgp config in hosts_vars
bgp playbook:
  - name: name of the task
  - name of the module (ios_l3_interface)
  
  - bgp conf  
     read from jinja template and create config
     
  - load conf   
    load conf from config folder
    
  -ios_command:
     commands:
        run commands (show ip int b)
     register: output (save output in variable)
    
    -name display output
     debug:
       var: output
    
    
