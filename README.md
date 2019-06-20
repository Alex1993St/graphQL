# graphQL
https://fostermade.co/blog/getting-started-with-graphql-in-laravel
https://auth0.com/blog/developing-and-securing-graphql-apis-with-laravel/
https://blog.hasura.io/building-progressive-todo-web-app-with-vuetify-vuex-graphql/
https://github.com/fostermadeco/laravel-graphql-blog
https://github.com/hasura/graphql-engine/tree/master/community/sample-apps/vuetify-vuex-todo-graphql
			return $this->query("INSERT INTO {$table} (" . implode(', ', array_keys($insert_field)) . ") VALUES ('" . implode("', '", array_values($insert_field)) . "')");
