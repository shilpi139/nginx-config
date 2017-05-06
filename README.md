# nginx-config

NGINX default file with 404 and 500 error pages.

# server-block
server {
	server_name iceAndFire.com www.iceAndFire.com;
	location / {
	  	root /home/shilpi/workspace/files/ice-and-fire;
	  	index index.html;
	}
	
	error_page 404 /custom_404.html;

	location = /custom_404.html {
	 	root /home/shilpi/workspace/files/ice-and-fire;
		internal;
	}
    
    error_page 500 501 502 503 504 /custom_500.html;
    
	location = /custom_500.html {
		root /home/shilpi/workspace/files/ice-and-fire;
		internal;
	}

}

