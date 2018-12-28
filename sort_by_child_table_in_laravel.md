```PHP
\App\Parent::with('child')
    ->select(‘child.*', \DB::raw('(SELECT column FROM child_table WHERE parent_table.child_id = child.id ) as sort'))
    ->orderBy('sort')
    ->get(); 
```
