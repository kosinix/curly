# Curly
A simple no-nonsense CURL wrapper in PHP

## Installation

 1. Download zip and extract.
 2. Require the autoload file:

    require_once 'path/to/curly/src/autoload.php';


## Usage

### Get

    use Curly\Curl;
    
    $curl = new Curl();
    $result = $curl->get('http://www.google.com');
    
    if($result->isError()){
    	var_dump($result->httpCode);
    	var_dump($result->error);
    } else {
    	echo $result; // Uses __tostring()
    	// or echo $result->result;
    }

### Post

    use Curly\Curl;
    
    $curl = new Curl();
    $result = $curl->post('http://www.google.com', array(
        'field1' => 'value'
    ));
    
    if($result->isError()){
    	var_dump($result->httpCode);
    	var_dump($result->error);
    } else {
    	echo $result; // Uses __tostring()
    	// or echo $result->result;
    }