Wordpress
=========

Install Wordpress.

Requirements
------------
None.

Role Variables
--------------

```yml
# Mariadb root password
wordpress_db_root_password: root00
# Wordpress db user(wordpress) password.
wordpress_db_password: wordpress00

# mariadb tuning 
wordpress_mysql_buffer_pool_size: 128M 
wordpress_mysql_log_file_size: 48M
wordpress_mysql_io_capacity: 200 
wordpress_mysql_io_capacity_max: 4000
wordpress_mysql_thread_cache_size: 10
wordpress_mysql_flush_log_at_trx_commit: 2
wordpress_mysql_doublewrite: 0
wordpress_mysql_max_connections: 100

# php tuning
wordpress_php_max_execution_time: 100
wordpress_php_memory_limit: 512M
wordpress_php_post_max_size: 128M
wordpress_php_upload_max_size: 128M
wordpress_php_max_input_time: 100
wordpress_php_max_input_vars: 300
wordpress_php_date_timezone: Asia/Tokyo

# wordpress download url
wordpress_targz_url: https://ja.wordpress.org/latest-ja.tar.gz

# wordpress blog url.
wordpress_url: "http://{{ inventory_hostname }}/wordpress"
# wordpress blog title.
wordpress_blog_title: "KICK-ASS"
# wordpress admin user name.
wordpress_admin_user: "admin"
# wordpress admin user password.
wordpress_admin_pass: "admin00"
# wordpress admin user email address.
wordpress_admin_email: "admin@localhost.localdomain"
```

Dependencies
------------
None.

Example Playbook
----------------
```yml
- hosts: linux_servers
  become: yes
  roles:
    - wordpress
```


License
-------

MIT

Author Information
------------------
https://github.com/sy4may0
