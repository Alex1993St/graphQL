# graphQL
https://fostermade.co/blog/getting-started-with-graphql-in-laravel
https://auth0.com/blog/developing-and-securing-graphql-apis-with-laravel/
https://blog.hasura.io/building-progressive-todo-web-app-with-vuetify-vuex-graphql/
https://github.com/fostermadeco/laravel-graphql-blog
https://github.com/hasura/graphql-engine/tree/master/community/sample-apps/vuetify-vuex-todo-graphql
return $this->query("INSERT INTO {$table} (" . implode(', ', array_keys($insert_field)) . ") VALUES ('" . implode("', '", array_values($insert_field)) . "')");
			
// Init cURL
$ch = curl_init();
curl_setopt($ch, CURLOPT_HEADER, 0);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, 0);

// Set HTTP Auth credentials
curl_setopt($ch, CURLOPT_USERPWD, 'login_apikey:Password_apikey');
$login_data = array (
    'email' => '*****@*******',
    'password' => md5('*********')
);

// Login
curl_setopt($ch, CURLOPT_URL, 'https://somesite.com/index/login');
curl_setopt($ch, CURLOPT_POSTFIELDS, $login_data);
$result = curl_exec($ch);
$data = json_decode($result,true);
