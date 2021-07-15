# Make buld
make-build:
	# admin_users
	cp ../admin_users/requirements.txt ./build/admin_users
	docker-compose build admin_users
	rm ./build/admin_users/requirements.txt

	# users_view
	cp ../users-view/package-lock.json ./build/users_view
	cp ../users-view/package.json ./build/users_view
	docker-compose build users_view
	rm ./build/users_view/package.json
	rm ./build/users_view/package-lock.json

start:
	docker-compose up -d