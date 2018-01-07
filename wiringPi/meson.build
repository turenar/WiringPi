pi_srcs = [
	'ads1115.c',
	'bmp180.c',
	'drcNet.c',
	'drcSerial.c',
	'ds18b20.c',
	'htu21d.c',
	'max31855.c',
	'max5322.c',
	'mcp23008.c',
	'mcp23016.c',
	'mcp23017.c',
	'mcp23s08.c',
	'mcp23s17.c',
	'mcp3002.c',
	'mcp3004.c',
	'mcp3422.c',
	'mcp4802.c',
	'pcf8574.c',
	'pcf8591.c',
	'piHiPri.c',
	'piThread.c',
	'pseudoPins.c',
	'rht03.c',
	'sn3218.c',
	'softPwm.c',
	'softServo.c',
	'softTone.c',
	'sr595.c',
	'wiringPi.c',
	'wiringPiI2C.c',
	'wiringPiSPI.c',
	'wiringSerial.c',
	'wiringShift.c',
	'wpiExtensions.c',
]

cc = meson.get_compiler('c')
m_dep = cc.find_library('m')
pthreads_dep = dependency('threads')
rt_dep = cc.find_library('rt')
crypt_dep = cc.find_library('crypt')

library('wiringpi', pi_srcs,
	dependencies: [m_dep, pthreads_dep, rt_dep, crypt_dep],
	c_args: ['-D_GNU_SOURCE'],
	include_directories: include_directories(['.']))
