### iostream # IOStream #> IOStream {tpl-git PHPDaemon/Network/IOStream.php}

```php
namespace PHPDaemon\Network;
abstract class IOStream;
```

@TODO

<!-- include-namespace path="\PHPDaemon\Network\IOStream" level="" access="" -->
#### consts # Constants

<md:const>
Alias of STATE_STANDBY
const STATE_ROOT = 0
</md:const>

<md:const>
Standby state (default state)
const STATE_STANDBY = 0
</md:const>

<div class="clearboth"></div>

#### properties # Properties

<md:prop>
/**
	 * @var object Associated pool
	 */
public $pool
</md:prop>

<div class="clearboth"></div>

#### methods # Methods

<md:method>
/**
	 * IOStream constructor
	 * @param resource $fd   File descriptor. Optional
	 * @param object   $pool Pool. Optional
	 */
public function __construct($fd = null, $pool = null)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L164
</md:method>

<md:method>
/**
	 * Getter
	 * @param  string $name Name
	 * @return mixed
	 */
public function __get($name)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L201
</md:method>

<md:method>
/**
	 * Freed?
	 * @return boolean
	 */
public function isFreed()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L216
</md:method>

<md:method>
/**
	 * Finished?
	 * @return boolean
	 */
public function isFinished()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L224
</md:method>

<md:method>
/**
	 * Get EventBufferEvent
	 * @return EventBufferEvent
	 */
public function getBev()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L232
</md:method>

<md:method>
/**
	 * Get file descriptor
	 * @return resource File descriptor
	 */
public function getFd()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L240
</md:method>

<md:method>
/**
	 * Sets context mode
	 * @param  object  $ctx  Context
	 * @param  integer $mode Mode
	 * @return void
	 */
public function setContext($ctx, $mode)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L251
</md:method>

<md:method>
/**
	 * Sets fd
	 * @param  resource $fd  File descriptor
	 * @param  object   $bev EventBufferEvent
	 * @return void
	 */
public function setFd($fd, $bev = null)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L262
</md:method>

<md:method>
/**
	 * Set timeout
	 * @param  integer $rw Timeout
	 * @return void
	 */
public function setTimeout($rw)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L333
</md:method>

<md:method>
/**
	 * Set timeouts
	 * @param  integer $read  Read timeout in seconds
	 * @param  integer $write Write timeout in seconds
	 * @return void
	 */
public function setTimeouts($read, $write)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L343
</md:method>

<md:method>
/**
	 * Sets priority
	 * @param  integer $p Priority
	 * @return void
	 */
public function setPriority($p)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L356
</md:method>

<md:method>
/**
	 * Sets watermark
	 * @param  integer|null $low  Low
	 * @param  integer|null $high High
	 * @return void
	 */
public function setWatermark($low = null, $high = null)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L367
</md:method>

<md:method>
/**
	 * Reads line from buffer
	 * @param  integer     $eol EOLS_*
	 * @return string|null
	 */
public function readLine($eol = null)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L389
</md:method>

<md:method>
/**
	 * Drains buffer
	 * @param  integer $n Numbers of bytes to drain
	 * @return boolean    Success
	 */
public function drain($n)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L401
</md:method>

<md:method>
/**
	 * Drains buffer it matches the string
	 * @param  string       $str Data
	 * @return boolean|null      Success
	 */
public function drainIfMatch($str)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L410
</md:method>

<md:method>
/**
	 * Reads exact $n bytes of buffer without draining
	 * @param  integer $n Number of bytes to read
	 * @param  integer $o Offset
	 * @return string|false
	 */
public function lookExact($n, $o = 0)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L442
</md:method>

<md:method>
/**
	 * Prepends data to input buffer
	 * @param  string  $str Data
	 * @return boolean      Success
	 */
public function prependInput($str)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L457
</md:method>

<md:method>
/**
	 * Prepends data to output buffer
	 * @param  string  $str Data
	 * @return boolean      Success
	 */
public function prependOutput($str)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L469
</md:method>

<md:method>
/**
	 * Read from buffer without draining
	 * @param integer $n Number of bytes to read
	 * @param integer $o Offset
	 * @return string|false
	 */
public function look($n, $o = 0)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L482
</md:method>

<md:method>
/**
	 * Read from buffer without draining
	 * @param  integer $o Offset
	 * @param  integer $n Number of bytes to read
	 * @return string|false
	 */
public function substr($o, $n = -1)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L498
</md:method>

<md:method>
/**
	 * Searches first occurence of the string in input buffer
	 * @param  string  $what  Needle
	 * @param  integer $start Offset start
	 * @param  integer $end   Offset end
	 * @return integer        Position
	 */
public function search($what, $start = 0, $end = -1)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L512
</md:method>

<md:method>
/**
	 * Reads exact $n bytes from buffer
	 * @param  integer      $n Number of bytes to read
	 * @return string|false
	 */
public function readExact($n)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L521
</md:method>

<md:method>
/**
	 * Returns length of input buffer
	 * @return integer
	 */
public function getInputLength()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L535
</md:method>

<md:method>
/**
	 * Called when the worker is going to shutdown
	 * @return boolean Ready to shutdown?
	 */
public function gracefulShutdown()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L543
</md:method>

<md:method>
/**
	 * Freeze input
	 * @param  boolean $at_front At front. Default is true. If the front of a buffer is frozen, operations that drain data from the front of the buffer, or that prepend data to the buffer, will fail until it is unfrozen. If the back a buffer is frozen, operations that append data from the buffer will fail until it is unfrozen
	 * @return boolean           Success
	 */
public function freezeInput($at_front = false)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L553
</md:method>

<md:method>
/**
	 * Unfreeze input
	 * @param  boolean $at_front At front. Default is true. If the front of a buffer is frozen, operations that drain data from the front of the buffer, or that prepend data to the buffer, will fail until it is unfrozen. If the back a buffer is frozen, operations that append data from the buffer will fail until it is unfrozen
	 * @return boolean           Success
	 */
public function unfreezeInput($at_front = false)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L565
</md:method>

<md:method>
/**
	 * Freeze output
	 * @param  boolean $at_front At front. Default is true. If the front of a buffer is frozen, operations that drain data from the front of the buffer, or that prepend data to the buffer, will fail until it is unfrozen. If the back a buffer is frozen, operations that append data from the buffer will fail until it is unfrozen
	 * @return boolean           Success
	 */
public function freezeOutput($at_front = true)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L577
</md:method>

<md:method>
/**
	 * Unfreeze output
	 * @param  boolean $at_front At front. Default is true. If the front of a buffer is frozen, operations that drain data from the front of the buffer, or that prepend data to the buffer, will fail until it is unfrozen. If the back a buffer is frozen, operations that append data from the buffer will fail until it is unfrozen
	 * @return boolean           Success
	 */
public function unfreezeOutput($at_front = true)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L589
</md:method>

<md:method>
/**
	 * Called when the connection is ready to accept new data
	 * @return void
	 */
public function onWrite()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L600
</md:method>

<md:method>
/**
	 * Send data to the connection. Note that it just writes to buffer that flushes at every baseloop
	 * @param  string  $data Data to send
	 * @return boolean       Success
	 */
public function write($data)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L608
</md:method>

<md:method>
/**
	 * Send data and appending \n to connection. Note that it just writes to buffer flushed at every baseloop
	 * @param  string  $data Data to send
	 * @return boolean       Success
	 */
public function writeln($data)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L633
</md:method>

<md:method>
/**
	 * Finish the session. You should not worry about buffers, they are going to be flushed properly
	 * @return void
	 */
public function finish()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L654
</md:method>

<md:method>
/**
	 * Close the connection
	 * @return void
	 */
public function close()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L677
</md:method>

<md:method>
/**
	 * Unsets pointers of associated EventBufferEvent and File descriptr
	 * @return void
	 */
public function unsetFd()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L695
</md:method>

<md:method>
/**
	 * Called when the connection has got new data
	 * @param  object $bev EventBufferEvent
	 * @return void
	 */
public function onReadEv($bev)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L714
</md:method>

<md:method>
/**
	 * Push callback which will be called only once, when writing is available next time
	 * @param  callable $cb Callback
	 * @return void
	 */
public function onWriteOnce($cb)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L751
</md:method>

<md:method>
/**
	 * Called when the connection is ready to accept new data
	 * @param  object $bev EventBufferEvent
	 * @return void
	 */
public function onWriteEv($bev)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L764
</md:method>

<md:method>
/**
	 * Called when the connection state changed
	 * @param  object  $bev    EventBufferEvent
	 * @param  integer $events Events
	 * @return void
	 */
public function onStateEv($bev, $events)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L812
</md:method>

<md:method>
/**
	 * Moves arbitrary number of bytes from input buffer to given buffer
	 * @param  \EventBuffer $dest Destination nuffer
	 * @param  integer      $n    Max. number of bytes to move
	 * @return integer|false
	 */
public function moveToBuffer(\EventBuffer $dest, $n)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L847
</md:method>

<md:method>
/**
	 * Moves arbitrary number of bytes from given buffer to output buffer
	 * @param  \EventBuffer $src Source buffer
	 * @param  integer      $n   Max. number of bytes to move
	 * @return integer|false
	 */
public function writeFromBuffer(\EventBuffer $src, $n)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L860
</md:method>

<md:method>
/**
	 * Read data from the connection's buffer
	 * @param  integer      $n Max. number of bytes to read
	 * @return string|false    Readed data
	 */
public function read($n)
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L872
</md:method>

<md:method>
/**
	 * Reads all data from the connection's buffer
	 * @return string Readed data
	 */
public function readUnlimited()
link:https://github.com/kakserpom/phpdaemon/blob/master/PHPDaemon/Network/IOStream.php#L890
</md:method>

<div class="clearboth"></div>


<!--/ include-namespace -->
