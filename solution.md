1. The HTTP Verb and URL (ie 'GET '/dogs'')
2. The rails controller action (ie 'dogs#index')
3. The corresponding CRUD action (ie 'READ)
4. The corresponding ActiveRecord method (ie 'all')


Display all the projects 

1. GET '/projects'
2. 'projects#index'
3. READ 
4. Project.all / 'SELECT * FROM projects'

Displays information about one project

1. GET '/projects/:id'
2. 'projects#show'
3. READ
4. Project.find(params[:id]) / 'SELECT * FROM projects WHERE id = ? '

Creates a new project based on given parameters
1. POST '/projects'
2. 'projects#create'
3. CREATE 
4. Project.create(project_params) / 'INSERT INTO projects VALUES (?)'

Updates an existing project with given parameters
1. PATCH '/porjects/:id'
2. 'projects#update'
3. UPDATE 
4. project = Project.find(params[:id]), project.update(project_params) / 'SELECT * FROM projects WHERE id = ? UPDATE products SET () WHERE id = ?'

Deletes an existing project
1. DELETE '/projects:id'
2. 'projects#destroy'
3. DELETE
4. project = Project.find(params[:id]), project.destroy / 'DELETE from projects WHERE id = ?'