```PHP
Parent::with('child')
    ->select(‘child.*', \DB::raw('(SELECT column FROM child_table WHERE parent_table.child_id = child.id ) as sort'))
    ->orderBy('sort')
    ->get(); 
```
another way

```PHP
Model::with('relation')->get()->sortBy(function($model){
    $model->relation->field_name;
});

Real Example:
AccountPassiveInvoice::with('supplier')->whereIn('payment_status',[0,2])->get()->sortBy(function ($due_invoice){
    return $due_invoice->supplier->supplier_company;
});
```
