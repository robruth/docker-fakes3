# docker-fakes3

Current Version: v0.2.1

## run fakes3

	docker run --name fakes3 -d -p 3128:3128 robruth/fakes3
	
## s3cmd on osx

	git clone https://github.com/s3tools/s3cmd.git
	python setup.py install
	sudo python setup.py install
	vi ~/.s3cfg
	
	Example config:
	
	https://gist.github.com/robruth/c7a92bc8ed0b182d97c4

	- Edit domain to reflect your own
	- Edit /etc/hosts or add DNS to resolve <bucket>.<domain>.com to Docker host IP
	
	Make a bucket:
	s3cmd mb s3://<bucket>
	
	Put a file:
	s3cmd put <file> s3://<bucket>/<filename>

	List a bucket:
	s3cmd ls s3://<bucketname>
