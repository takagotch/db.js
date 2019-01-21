### db.js
---
https://github.com/aaronpowell/db.js/

```
<script src='/dist/db.js'></script>
```

```js
var server;
db.open({
  server: 'my-app',
  version: 1,
  schema: {
    people: {
      key: {keyPath: 'id', autoIncrement: true},
      indexes: {
        firstName: {},
        answer: {unique: true}
      }
    }
  }
}).then(function(s){
  server = s;
});

var server;
db.open({
}).catch(function(err){
  if(err.type === 'blocked'){
    oldConnection.close();
    return err.resume;
  }
  throw err;
}).then(function(s){
  server = s;
});

server.people.add({
  firstName: 'Aaron',
  lastName: 'Powell',
  answer: 42
}).then(function(item){
});

server.people.update({
  fistName: 'Aaron',
  lastName: 'Powell',
  answer: 42
}).then(function(item){
});

server.people.remove(1).then(function(key){
});

server.people.clear()
  .then(function(){
  });
  
server.people.get(5)
  .then(function(results){
  });
  
server.people.get({gte: 1, lt: 3})
  .then(function(results){
  });

server.people.get(IDBKeyRange.bound(1, 3, false, true))
  .then(function(results){
  });
  
server.people.query()
  .all()
  .execute()
  .then(function(result){
  });
  
server.people.query('specailProperty')
  .all()
  .execute()
  .then(funcion(results){
  });
  
server.people.query()
  .filter('firstname', 'Aaron')
  .execute()
  .then(function(results){
  });
  
server.people
  .query('firstName')
  .only('Aaron')
  .distinct()
  .then(function (date){
  });
  
server.people.query('firstName')
  .only('Aaron')
  .then(function(results){
  });
server.people.query('answer')
  .bound(30, 50)
  .then(function(results){
  });
  
server.people.query('firstname')
  .range({eq: 'Aaron'})
  .then(function(results){
  });

server.people.query('answer')
   .range({gte: 30, lte: 50})
   .then(function(results){
   });
   
schema: {
  people: {
    key: {
      keyPath: ['lastName', 'firstName']
    },
    indexes: {
      name: {
        keyPath: ['lastName', 'firstName']
      },
      lastName: {},
      firstName: {}
    }
  }
}
s.test.query('name')
  .only(['Zamir', 'Brett'])
  .execute()
  .then(function(results){
  });

server.people
  .query('firstname')
  .all()
  .limit(1, 3)
  .execute()
  .then(function(data){
  });
  
server.people.query()
  .all()
  .desc()
  .execute()
  .then(function(results){
  });
  
server.people.query('firstName')
  .only('Aaron')
  .keys()
  .execute()
  .then(function(results){
  });
  
server.people
  .query('age')
  .lowerBound(30)
  .map(function(value){
    return{
      fullName: value.firstName + ' ' + value.lastName,
      raw: value
    };
  })
  .execute()
  .then(function(data){
  });
  
server.people.query('firstName')
  .only('Aaron')
  .count()
  .execute()
  .then(funciton(results){
  });
  
server.people.count().then(function(ct){
});

server.people.count(myKey).then(function(ct){
});
server.people.count({gte: 1, lt: 3}).then(function(ct){
});
server.people.count(IDBKeyRange.bound(1, 3, false, true)).then(function(ct){
});

server.users.query('last_mod')
  .lowerBound(new Date().getTime() - 10000)
  .modify({last_mod: new Date.getTime()})
  .execute()
  .then(function(results){
  });
server.users.query('changed')
  .only(true)
  .modify({changed: false})
  .execute
  .then()
server.profiles.query('name')
  .lowerBound('marcy')
  .modify({views: function(profile){ return profile.views + 1; }})
  .execute()
  .then()
  
server.close();

var db = server.getIndexedDB();
var storeNames = db.objectStoreNames;

server.addEventListener('abort', function(e){
});
server.addEventListener('error', function(e){
});
server.addEventListener('versionchange', function(e){
});

server.abort(function(e){
}).error(function(err){
})/versionchange(function(e){
});

db.delete(dbName).then(function(ev){
}, function(err){
});

db.delete(dbName).catch(function(err){
  if(err.type === 'blocked'){
    oldConnection.close();
    return err.resume;
  }
  throw err;
}).then(function(ev){
});

db.cmp(key1, key2).then(function(ret){
});
```

```
```

