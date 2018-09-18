Dans le code suivant identifiez les différentes erreurs s'y trouvant

```
class Foo
{

	/**
	 * @param string $param
	 * @param $somethingElse
	 * @return bool
	 */
	function bar($param) {
	  $this->bar($param);

		if ($param = 0) {
			return false;
		} else {
			return true;
		}
			return true;
	}

	/**
	 * @param $firstParam
	 * @param $second_param
	 * @return mixed
	 */
	public function baz($firstParam, $second_param)
	{
		return $second_param;
	}
  
  /**
   * @param string $status
   */
  function isStatusAll($status) 
  {
      return ($status != 'all');
  }
}
```
